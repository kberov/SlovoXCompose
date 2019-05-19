<div>
    <style>
    @font-face {
        font-family: 'Veleka';
        src: url('fonts/veleka-regular-webfont.woff2') format('woff2');
        font-weight: normal;
        font-style: normal;
    }

    @font-face {
        font-family: 'Veleka';
        src: url('fonts/veleka-bolditalic-webfont.woff2') format('woff2');
        font-weight: bold;
        font-style: italic;
    }

    @font-face {
        font-family: 'Veleka';
        src: url('fonts/veleka-italic-webfont.woff2') format('woff2');
        font-weight: normal;
        font-style: italic;
    }

    @font-face {
        font-family: 'Veleka';
        src: url('fonts/veleka-bold-webfont.woff2') format('woff2');
        font-weight: bold;
        font-style: normal;
    }

    @font-face {
        font-family: 'FreeSerif';
        src: url('fonts/freeserif-webfont.woff2') format('woff2');
        font-weight: normal;
        font-style: normal;
    }

    @font-face {
        font-family: 'FreeSans';
        src: url('fonts/freesans-webfont.woff2') format('woff2');
        font-weight: normal;
        font-style: normal;
    }

    @font-face {
        font-family: 'FreeMono';
        src: url('fonts/freemono-webfont.woff2') format('woff2');
        font-weight: normal;
        font-style: normal;
    }

    @font-face {
        font-family: 'BukyvedeRegular';
        src: url('fonts/bukyvede-regular-webfont.woff2') format('woff2');
        font-weight: normal;
        font-style: normal;
    }

    @font-face {
        font-family: 'BukyvedeRegular';
        src: url('fonts/bukyvede-bold-webfont.woff2') format('woff2');
        font-weight: bolder;
        font-style: normal;
    }

    /* Generic font styles */
    h1,h2,h3,h4,p {
        font-family: Veleka, BukyvedeRegular, FreeSerif, serif;
        font-weight: normal;
    }
    </style>
</div>

# ИМѦ

SlovoXCompose

# БѢЛѢЖКА

Правописѫт и словникѫт, използувани в това рѫководство сѫ просто пример за употрѣба
на старитѣ букви и не сѧ твърди, че сѧ спазват каквито и да е правила, макар
да отразѣват до нѣкаква стѫпен (само)мнѣнието на пишещѭ.

# ОПИСАНѤ

Това хранилище съдържа файл `.XCompose` с настройки за _съставно въвѣжданѣ_
на стари български бꙋкви на Юниѯ-подобни ꙋрѣдби с Ѯ-сървър. Такива изчислителни
ꙋредби сѫ всички изданиꙗ на Линуѯ, Фрий-БСД, НЕТ-БСД… Това е възможно
най-леснo осѫществимѭт начин да започнетѣ да въвѣждатѣ бꙋкви ѿ старата ни
азбꙋка. Разбира сѧ, би било добрѣ да има и по-добър, по-бърз начин. Има, но той
все още не сѫществува (в прѣдставителен вид). Ако имахме утвърдена клавиатурна
подредба, то това би било този по-добър начин. Уверꙗвѫ ви, че вече една скꙋпина
съмишленици работи по въпроса, макар да е само умствено засѣга.

Прѣдимството на тук прѣдложенѭ начин е в това, че можетѣ лѣсно да добавитѣ нови
собствени послѣдователности ѿ знаци, които при въвѣжданѣ да изобразѣватъ на
екранѫ и в документитѣ ви опрѣдѣлени букви, както и че лесно можете да се
досетите каква би била послѣдователността от знаци, която трѣбва да въвѣдетѣ,
за да се изобрази опрѣдѣлен знак. Този начин е добър при спорадично въвѣжданѣ
на стари бꙋкви. Ако сѧ чудитѣ, как сѧ въвѣжда нѣкой знак, то просто ѿворетѣ
`.XCompose` в сѫщата папка, кѫдѣто е и този файл, и пѿърсете в нѣго.

В случай че сѧ занимаватѣ с такива писаниꙗ като занаꙗтчꙗ или по призванѥ, то
може би е по-добре да ползуватѣ клавꙗтурна подрѣдба – звꙋкова или по БДС.(Все
още нѣма такава създадена.)

# ВНѢДРѢВАНЕ

Ꙁасѣга внѣдрѣването е рѫчно. Требва да прочететѣ ꙋказанията по-долу. При нѣкое
следващо изданѥ, ще предоставим и програма, която да го прави вмѣсто вас. Всѣ
пак е добре да знаете как рабѿи.

# ꙊКАЗАНꙖ

## Какъ рабѿи `.XCompose`?

В Юниѯ-подобнитѣ урѣдби сѧ ползуват най-чѧсто двѣ изобразѣващи работни срѣди –
KDE или GNOME. Тези срѣди използуват свои собствени книговни за изобразѣване на
прозорци, копчета и други видими нагодѣ. Общо вꙁѣто тези дветѣ (Qt и GTK+)
книговни сѫ най-използуванитѣ и сѧ използуватъ и ѿ други рабѿни срѣди като
XFCE, LXQT, LXDE, както и ѿ всѣко по-важно приложенѥ.

За да използуват този файл програмите, изобразѣващи тваритѣ си с помощта на
гореупомѣнатитѣ две книговни, първо трѣбва да сѧ присвои една опрѣдѣлена
стойност на две промѣнливи на обкрѫженѥто ето така:

    export GTK_IM_MODULE="gtk-im-context-simple"
    export QT_IM_MODULE="gtk-im-context-simple"

Поставетѣ горнитѣ двѣ опрѣдѣленꙗ въ файла `~/.profile`. Така винаги, когато
влизатѣ въ вашата рабѿнa срѣда, тези промѣнливи ще ꙋказват на приложенꙗта да
зарѣждат файла `~/.XCompose` или ꙋказанѭ файл въ стойността на промѣнливата на
обкрѫженѥто `$XCOMPOSEFILE`. 

Сиреч, можетѣ или просто да поставитѣ този `.XCompose` в домашната си папка,
или въ `~/.profile` да добавитѣ и слѣднѭ рѣд (примѣр):

    export XCOMPOSEFILE="$HOME/opt/dev/SlovoXCompose/.XCompose"

Замѣстетѣ пѫтѭ до файлѫ според това кѫдѣ се намира на вашата машина.
Това е. Излѣзтѣ и влѣзтѣ ѿново в рабѿната си срѣда, за да сѧ задействат промѣнитѣ.

## Как да въвѣждѫ старитѣ бꙋкви?

Преди да можетѣ да въвѣждатѣ стари бꙋкви само с помощта на клавꙗтурата, е
необходимо да зададетѣ/ꙋкажетѣ/настроитѣ вашиѭ _Съставен клавиш_ (Compose key).
На съвремѩните клавиатури нѣма такъв клавиш, така че трѣбва да си изберетѣ
нѣкой рѣдко използуван за други цели клавиш и да настроитѣ него. Въ файлѫ
`/usr/share/X11/xkb/rules/xorg.lst` има пълен списък с възможнитѣ клавиши.
Ето го.

    Compose key          Position of Compose key
    (Съставен)           (Мѣстоположенѥ на съставнѭ ключ)
    compose:ralt         Right Alt
    compose:lwin         Left Win
    compose:lwin-altgr   3rd level of Left Win
    compose:rwin         Right Win
    compose:rwin-altgr   3rd level of Right Win
    compose:menu         Menu
    compose:menu-altgr   3rd level of Menu
    compose:lctrl        Left Ctrl
    compose:lctrl-altgr  3rd level of Left Ctrl
    compose:rctrl        Right Ctrl
    compose:rctrl-altgr  3rd level of Right Ctrl
    compose:caps         Caps Lock
    compose:caps-altgr   3rd level of Caps Lock
    compose:102          &lt;Less/Greater&gt;
    compose:102-altgr    3rd level of &lt;Less/Greater&gt;
    compose:paus         Pause
    compose:prsc         PrtSc
    compose:sclk         Scroll Lock

Този списък може да сѧ види в графичните настройки за клавиатурата
в KDE, GNOME, XFCE…

<div>
    <img src="img/kompose_key_2019-05-05_20-56-42.png" width="800">
</div>

Допълнително (в настройкитѣ за трето ниво) ще видитѣ:

    lv3:ralt_switch_multikey Right Alt; Shift+Right Alt as Compose

Аз прѣдпочитам нѣго.

XFCE нѣма отделни настройки за трето ниво, но тази стойност може да се зададе
чрѣз т.нар. „Редактор на настройкитѣ“. Ето как изглежда.

<div>
    <img src="img/ralt_switch_multikey.png" width="800">
</div>

Така в XFCE можетѣ хем да зададетѣ _Съставен ключ_, хем да зададетѣ клавиш
(ключ) за трето ниво. Ключът за трето ниво се използува в други случаи.

> **Самото въвѣждане става по слѣднѭ начин:**
>
> Нaтискате избранѭ _съставен ключ_ (Compose). Пускате го. Не го държите
> постоянно натиснат. Слѣд това въвѣждате първата, а след неꙗ и втората бꙋква ѿ
> послѣдователността.
>
> Примѣр (за съставен ключ е избран Shift+Right Alt):
>
> > Ꙁа да въвѣдетѣ „ѯ” като в „Линуѯ”, натискате едновременно Shift и десен Alt, а
> > след това натискате послѣдователно „к” и „с”.
> >
> > Ꙁа да напишете „ꙁемꙗ”, натискате едновременно Shift и десен Alt, а след това
> > натискате послѣдователно „з” и „е”. Слѣд това продължавате съ „ем”. След което,
> > ꙁа да напишете ꙗ, правите както при ꙁ – натискате едновременно Shift и десен
> > Alt, а след това натискате послѣдователно „и” и „а”.
>
> А ето и всички определени в този .XCompose съчетания за въвѣждане. „`||`”
> означава „`или`”:

    Compose,З,E => Ꙁ
    Compose,з,e => ꙁ
    Compose,З,З => S
    Compose,з,з => s
    Compose,Д,З => Ꙃ
    Compose,д,з => ꙃ
    Compose,И,. => І || Compose,.,И => І
    Compose,и,. => і || Compose,.,и => і
    Compose,И,: => Ї || Compose,:,И => Ї
    Compose,и,: => ї || Compose,:,и => ї
    Compose,О,У => Ѹ || Compose,У,О => Ѹ || Compose,У,о => Ѹ || Compose,О,у => Ѹ
    Compose,о,у => ѹ
    Compose,У,К => Ꙋ || Compose,У,к => Ꙋ
    Compose,у,к => ꙋ
    Compose,О,М => Ѡ || Compose,О,м => Ѡ
    Compose,о,м => ѡ
    Compose,Я,Е => Ѣ || Compose,Е,Я => Ѣ
    Compose,я,е => ѣ || Compose,е,я => ѣ
    Compose,И,А => Ꙗ || Compose,И,а => Ꙗ
    Compose,и,а => ꙗ
    Compose,И,Е => Ѥ
    Compose,и,е => ѥ
    Compose,Е,Н => Ѧ || Compose,А,Н => Ѧ || Compose,Е,н => Ѧ || Compose,А,н => Ѧ
    Compose,е,н => ѧ || Compose,a,н => ѧ
    Compose,И,Н => Ѩ || Compose,Я,Н => Ѩ || Compose,И,н => Ѩ || Compose,Я,н => Ѩ
    Compose,и,н => ѩ || Compose,я,н => ѩ
    Compose,Ъ,Н => Ꙙ || Compose,Ъ,н => Ꙙ
    Compose,ъ,н => ꙙ
    Compose,Й,Н => Ꙝ || Compose,Й,н => Ꙝ
    Compose,й,н => ꙝ
    Compose,Е,М => Ѫ || Compose,Е,м => Ѫ || Compose,А,м => Ѫ || Compose,А,М => Ѫ
    Compose,Ъ,А => Ѫ || Compose,А,Ъ => Ѫ || Compose,Ъ,а => Ѫ || Compose,А,ъ => Ѫ
    Compose,е,м => ѫ || Compose,а,м => ѫ
    Compose,ъ,а => ѫ || Compose,а,ъ => ѫ
    Compose,И,М => Ѭ || Compose,Я,М => Ѭ || Compose,И,Я => Ѭ || Compose,И,я => Ѭ
    Compose,и,м => ѭ || Compose,и,я => ѭ
    Compose,И,Ъ => Ѭ || Compose,И,ъ => Ѭ
    Compose,и,ъ => ѭ
    Compose,К,С => Ѯ
    Compose,к,с => ѯ
    Compose,П,С => Ѱ
    Compose,п,с => ѱ
    Compose,Т,Х => Ѳ || Compose,Т,Ф => Ѳ
    Compose,т,х => ѳ || Compose,т,ф => ѳ
    Compose,У,Ж => Ѵ || Compose,И,Ж => Ѵ
    Compose,у,ж => ѵ || Compose,и,ж => ѵ
    Compose,Ж,: => Ѷ
    Compose,ж,: => ѷ
    Compose,К,О => Ҁ
    Compose,к,о => ҁ
    Compose,О,Т => Ѿ
    Compose,о,т => ѿ
    Compose,И,И => Ы
    Compose,и,и => ы

# ПРИНОС

Можетѣ да помогнете като добавитѣ нови последователности ѿ клавиши или като
поправите неработещите вѣчѣ сѫществуващи такива. Новата послѣдователност ще
заработи слѣд като спрѣтѣ и пуснете приложенѥто (в което въвѣждатѣ бꙋквитѣ)
ѿново.

# СЪСТАВИЛ ТОВА РѪКОВОДСТВО

Красимир Беров <berov@cpan.org>

# СЪСТАВИЛ .XCompose

Красимир Беров
