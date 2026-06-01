---
{"dg-publish":true,"permalink":"/semester-4/knk/notes/"}
---


# KNK - Permbledhje per provim

> Burimet e lexuara: `Ligjerata/Ligjerata 1-13.pdf`, `Ligjerata/Syllabus.pdf`, `Ligjerata/Përmbledhje_Detyrash_KNK.pdf`, si dhe materiali i vjeter ne `Ligjerata (Vjetra)` duke perfshire `Ligjerata_1...Ligjerata_13`, `KNK-Ushtrime.pdf`, `KnkTeori.docx.pdf`, `KnkTeori_1.pdf`, `KNK_Përmbledhje_Detyrash.pdf`.

## Rendi i materialit

Materiali i ri eshte renditur keshtu:

1. Njeriu ne HCI
2. Kompjuteri ne HCI
3. Interaksioni
4. Hyrje ne GUI dhe JavaFX
5. Property Binding dhe CSS ne JavaFX
6. Ngjyrat, teksti dhe imazhet
7. Panelet / layout panes
8. Shapes, Text, Label dhe figurat gjeometrike
9. Softueri i udhehequr nga ngjarjet
10. Klasat e brendshme dhe handler-at anonim
11. Paradigmat ne HCI
12. Bazat e dizajnit te interaksionit
13. HCI ne proceset e softuerit

Materiali i vjeter ka pothuajse te njejtat tema, por JavaFX fillon i pari dhe teorite e HCI vijne pas tij. Per provim, meso rendin e ri me siper, por perdor edhe ligjeratat e vjetra sepse kane formulime dhe shembuj qe perseriten.

---

## Ligjerata 1 - Njeriu ne HCI

### Ideja kryesore

HCI/KNK nuk studion vetem kompjuterin. Studion sistemin e plote: njeriun, kompjuterin, detyren dhe kontekstin ku perdoret sistemi. Dizajni i mire fillon nga kufizimet njerezore: si shohim, degjojme, levizim, mbajme mend, mesojme dhe bejme gabime.

### Pamja

Pamja ka dy gjendje:

- Marrja fizike e ngacmimit: syri pranon drite, ngjyra, levizje dhe kontrast.
- Perpunimi dhe interpretimi: truri i jep kuptim asaj qe syri pranon.

Kjo eshte arsyeja pse dy perdorues mund ta shohin te njejten nderfaqe, por ta kuptojne ndryshe. Iluzionet optike tregojne qe perceptimi nuk eshte fotografim i realitetit, por interpretim. Ne dizajn kjo do te thote: mos u mbeshtet vetem ne nje sinjal vizual; perdor kontrast, etiketa, pozicionim, feedback dhe hierarki.

### Degjimi

Degjimi jep informata per ambientin: drejtim, distance, objekte dhe ngjarje. Veshi ndahet ne:

- veshi i jashtem
- veshi i mesem
- veshi i brendshem

Zeri pershkruhet me frekuence, intensitet/zerim dhe ton. Ne nderfaqe, tingujt jane te dobishem per sinjale te shkurtra, por nuk duhet te jene menyra e vetme e komunikimit, sepse perdoruesi mund te jete ne ambient te zhurmshem ose me zhurmen e fikur.

### Levizja dhe koha e reagimit

Koha totale per te vepruar eshte:

```text
Koha e reagimit + Koha e levizjes
```

Koha e reagimit varet nga lloji i stimulit:

- pamje: rreth 200 ms
- zeri: rreth 150 ms
- dhimbja: rreth 700 ms

Koha e levizjes varet nga mosha, shendeti, aftesia motorike, pajisja dhe madhesia e objektivit. Ne GUI, butonat shume te vegjel, distancat e medha dhe objektivat pa tolerance rrisin gabimet.

### Memoria

Materiali dallon tre lloje kryesore:

- Memoria sensorike: ruan per shume pak kohe gjurmet e perceptimit.
- Memoria punuese / afatshkurter: perdoret gjate detyres aktuale.
- Memoria afatgjate: ruan njohuri, pervoja dhe modele mendore.

Memoria afatshkurter ka kapacitet te kufizuar, shpesh permendet si `7 ± 2` njesi. Kjo shpjegon pse numerat e gjate, listat e medha dhe menute pa grupim jane te veshtira. Teknikat si grupimi/chunking e ulin ngarkesen.

Shembull:

```text
Veshtire: 212348278493202
Me lehte: 212 348 278 493 202
```

### Te menduarit

Te menduarit perfshin:

- Rezonim deduktiv: nga rregulli i pergjithshem te rasti i vecante.
- Rezonim induktiv: nga raste te vecanta te nje pergjithesim.
- Rezonim rrembyes/abduktiv: zgjedh shpjegimin me te mundshem.
- Zgjidhje problemesh: perdoruesi kerkon rruge nga gjendja aktuale te caku.

Per dizajn kjo do te thote se sistemi duhet ta beje gjendjen te dukshme: ku jam, cfare mund te bej, cfare ndodhi, dhe si kthehem mbrapa.

### Pika per provim

- HCI e merr seriozisht kufizimin njerezor, jo vetem fuqine teknike.
- Perceptimi nuk eshte gjithmone i sakte; dizajni duhet te jete i qarte dhe redundant.
- Memoria afatshkurter eshte e kufizuar; perdor grupim, etiketa dhe default-e.
- Reagimi i shpejte dhe feedback-u ulin pasigurine e perdoruesit.

---

## Ligjerata 2 - Kompjuteri ne HCI

### Ideja kryesore

Per ta kuptuar interaksionin njeri-kompjuter duhet te kuptohet edhe kompjuteri: cfare hyn brenda, cfare del jashte, cfare mund te beje dhe cfare kufizimesh ka.

### Sistemi tipik kompjuterik

Nje sistem tipik ka:

- ekran/monitor ku shfaqen dritaret
- tastiere per tekst dhe komanda
- mi ose pajisje treguese
- pajisje ruajtjeje dhe perpunimi
- variante si desktop, laptop, telefon, tablet, PDA, pajisje te integruara

Kompjuteret nuk jane vetem PC. Materiali permend pajisje ne shtepi dhe xhep: TV, DVD, mikrovale, makina larese, sisteme sigurie, telefona, kamera, smart kartela, qelesa elektronik, USB etj. Kjo eshte e rendesishme sepse HCI aplikohet kudo ku ka sistem interaktiv.

### Pajisjet hyrese

Pajisjet per vendosje teksti:

- tastiera tradicionale
- tastiera virtuale
- njohja e shkrimit
- njohja e zerit

Pajisjet per pozicionim dhe tregim:

- mouse
- touchpad
- touchscreen
- stylus
- joystick
- trackball

Zgjedhja e pajisjes ndikon ne shpejtesi, saktesi dhe lodhje. Per shembull, mouse eshte i mire per perzgjedhje te sakta ne desktop, touchscreen eshte i natyrshem per pajisje mobile, ndersa tastiera eshte me e shpejte per tekst te gjate.

### Pajisjet dalese

Dalja mund te jete:

- vizuale: monitor, projektor, ekrane mobile
- audio: zera, alarme, feedback zanor
- haptike: vibrim, force feedback
- printim ose output fizik

Ekrani ka rendesi te madhe: madhesia, rezolucioni, kontrasti, refresh rate dhe ngjyrat ndikojne ne perdorshmeri. Nga materiali i vjeter permendet si shembull rezolucioni SVGA `1024 x 768` dhe rezolucione me te medha moderne.

### Rreziqe dhe ergonomi

Materiali i vjeter permend edhe rreziqe shendetesore nga CRT, si rrezatim X dhe UV. Sot kjo eshte me pak problem me ekrane moderne, por parimi mbetet: HCI perfshin edhe sigurine, lodhjen, pozicionin e trupit, ndricimin, distancen e ekranit dhe pushimet.

### Pika per provim

- HCI duhet te pershtatet me pajisjen, jo vetem me programin.
- Input dhe output jane pjese e eksperiences se perdoruesit.
- Nderfaqja e mire merr parasysh rezolucionin, madhesine e ekranit, pajisjen hyrese dhe kontekstin.
- Pajisjet mobile dhe te integruara e zgjerojne HCI pertej desktop-it.

---

## Ligjerata 3 - Interaksioni

### Cfare eshte interaksioni?

Interaksioni eshte komunikimi midis perdoruesit dhe sistemit. Nuk eshte vetem klikim butonash. Eshte proces ku perdoruesi ka nje qellim, formulon veprime, i kryen ne nderfaqe, sheh rezultatin dhe e interpreton.

### Terma kryesore

- Domeni: hapesira e punes qe studiohet. Shembull: dizajni grafik, sistemi bankar, menaxhimi i studenteve.
- Caku: ajo qe perdoruesi deshiron te arrije.
- Puna/detyra: si realizohet caku me veprime konkrete.
- Qellimi: formulim me i afert me ate qe perdoruesi do te beje ne sistem.
- Aksioni: veprim fizik ose logjik ne nderfaqe, p.sh. klikim, zgjedhje menuje, shtypje teksti.

### Modeli i Norman-it

Modeli i Norman-it ka shtate faza:

1. Perdoruesi percakton cakun.
2. Formulon qellimin.
3. Percakton aksionet ne interfejs.
4. Ekzekuton aksionet.
5. Percepton gjendjen e sistemit.
6. Interpreton gjendjen.
7. Vlereson nese caku u arrit.

Ky model tregon dy hendeke:

- Hendeku i ekzekutimit: sa e veshtire eshte per perdoruesin ta ktheje qellimin ne veprim.
- Hendeku i vleresimit: sa e veshtire eshte ta kuptoje rezultatin pas veprimit.

Nderfaqja e mire i zvogelon te dyja. Shembull: nje buton `Save` me ikone dhe feedback `Saved` zvogelon hendekun e ekzekutimit dhe vleresimit.

### Stilet e interaksionit

Nga materiali teorik:

- Command line interface: perdoruesi shkruan komanda. I fuqishem per eksperte, i veshtire per fillestare.
- Menu-based interface: perdoruesi zgjedh nga opsione te dukshme.
- Form fill-in: perdoruesi ploteson fusha.
- Direct manipulation: perdoruesi manipulon objekte ne ekran, p.sh. drag and drop.
- Natural language: komunikim me fjali natyrore.
- GUI/WIMP: windows, icons, menus, pointer.

### Rregullat orientuese

Nga materiali i vjeter dalin kater ide praktike:

1. Dije ku je.
2. Dije cfare mund te besh.
3. Dije ku do te shkosh.
4. Dije ku ke qene.

Keto lidhen me navigation, breadcrumb, state, feedback, history dhe undo.

### Pika per provim

- Interaksioni eshte cikel komunikimi, jo vetem input.
- Modeli i Norman-it eshte shume i rendesishem per pyetje teorike.
- Hendeku i ekzekutimit ulet me affordance, etiketa, meny dhe controls te qarta.
- Hendeku i vleresimit ulet me feedback, status, error messages dhe vizualizim te gjendjes.

---

## Ligjerata 4 - Hyrje ne GUI dhe JavaFX

### JavaFX, Swing dhe AWT

Materiali e vendos JavaFX si teknologji moderne per GUI ne Java. Swing eshte perdorur shume per desktop, AWT eshte me i vjeter, ndersa Applet-at sot konsiderohen te pazbatueshem. Per lenden, fokusi eshte JavaFX.

### Modeli Stage - Scene - Node

JavaFX perdor analogjine e teatrit:

- `Stage`: dritarja kryesore.
- `Scene`: pamja/skena qe vendoset ne stage.
- `Node`: elementet brenda scene, si butona, label, forma, imazhe.
- `Pane`: container qe mban dhe organizon node.

Rrjedha tipike:

```text
Application -> start(Stage) -> krijo Node/Pane -> krijo Scene -> stage.setScene(scene) -> stage.show()
```

### Shembull baze JavaFX

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Label;
import javafx.scene.layout.StackPane;
import javafx.stage.Stage;

public class Main extends Application {
    @Override
    public void start(Stage stage) {
        Label label = new Label("Pershendetje KNK");
        StackPane root = new StackPane(label);

        Scene scene = new Scene(root, 400, 250);
        stage.setTitle("Aplikacioni i pare JavaFX");
        stage.setScene(scene);
        stage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
```

### Cfare duhet mbajtur mend

- `main` therrret `launch(args)`.
- `launch` nis JavaFX runtime.
- `start(Stage stage)` eshte pika kryesore ku ndertohet GUI.
- Stage nuk shfaqet derisa te thirret `show()`.

---

## Ligjerata 5 - Property Binding dhe CSS

### Property Binding

Binding do te thote lidhje midis vetive. Kur ndryshon nje vlere, vlera tjeter perditesohet automatikisht. Kjo eshte e dobishme ne GUI sepse madhesite, pozicionet dhe tekstet shpesh varen nga gjendja e aplikacionit.

Shembull: rrezja e rrethit lidhet me gjeresine e dritares.

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.layout.Pane;
import javafx.scene.paint.Color;
import javafx.scene.shape.Circle;
import javafx.stage.Stage;

public class BindingExample extends Application {
    @Override
    public void start(Stage stage) {
        Pane pane = new Pane();

        Circle circle = new Circle();
        circle.setFill(Color.LIGHTBLUE);
        circle.setStroke(Color.DARKBLUE);

        circle.centerXProperty().bind(pane.widthProperty().divide(2));
        circle.centerYProperty().bind(pane.heightProperty().divide(2));
        circle.radiusProperty().bind(pane.widthProperty().divide(6));

        pane.getChildren().add(circle);

        stage.setScene(new Scene(pane, 500, 300));
        stage.show();
    }
}
```

### CSS ne JavaFX

JavaFX mund te stilizohet me CSS, ngjashem me web. Materiali jep shembullin:

```java
circle.setStyle("-fx-stroke: black; -fx-fill: red;");
```

Ekuivalent me:

```java
circle.setStroke(Color.BLACK);
circle.setFill(Color.RED);
```

CSS eshte e mire kur duam ta ndajme stilin nga logjika. Kodi Java kontrollon sjelljen, CSS kontrollon pamjen.

### Shembull me stylesheet

```java
Scene scene = new Scene(root, 400, 250);
scene.getStylesheets().add(getClass().getResource("style.css").toExternalForm());
```

`style.css`:

```css
.primary-button {
    -fx-background-color: #2563eb;
    -fx-text-fill: white;
    -fx-font-weight: bold;
}
```

Ne Java:

```java
Button saveButton = new Button("Save");
saveButton.getStyleClass().add("primary-button");
```

### Pika per provim

- Binding e mban GUI te sinkronizuar me gjendjen.
- CSS ne JavaFX perdor prefiksin `-fx-`.
- `setStyle` eshte inline style; stylesheet eshte me i paster per projekte me te medha.

---

## Ligjerata 6 - Ngjyrat, teksti dhe imazhet

### Klasa Color

`Color` perdoret per te caktuar ngjyren e tekstit, shapes, background-it etj.

```java
circle.setFill(Color.RED);
circle.setStroke(Color.BLACK);
```

Mund te krijohen ngjyra edhe me RGB:

```java
Color custom = Color.rgb(30, 144, 255);
```

ose me transparence:

```java
Color transparentBlue = Color.rgb(30, 144, 255, 0.4);
```

### Teksti

JavaFX ka `Text` dhe `Label`.

- `Text` eshte node per shfaqje teksti dhe mund te stilohet si shape.
- `Label` eshte control per tekst jo te redaktueshem dhe perdoret shpesh me forms/buttons.

Shembull:

```java
Text title = new Text("KNK");
title.setFill(Color.DARKGREEN);
title.setStyle("-fx-font-size: 32px; -fx-font-weight: bold;");

Label label = new Label("Emri:");
label.setTextFill(Color.DARKSLATEGRAY);
```

### Image dhe ImageView

`Image` perfaqeson imazhin, `ImageView` e shfaq ate ne scene.

```java
Image image = new Image("file:src/main/resources/photo.png");
ImageView imageView = new ImageView(image);
imageView.setFitWidth(200);
imageView.setPreserveRatio(true);
```

Nese imazhi eshte ne resources:

```java
Image image = new Image(getClass().getResource("/photo.png").toExternalForm());
```

### Pika per provim

- `Color` perdoret per `fill`, `stroke`, `textFill`.
- `ImageView` kontrollon madhesine e shfaqjes, jo vetem ngarkimin e imazhit.
- `preserveRatio(true)` ruan proporcionet e imazhit.

---

## Ligjerata 7 - Layout Panes

### Ideja kryesore

Ne JavaFX, elementet shtohen ne `Pane`, pastaj `Pane` vendoset ne `Scene`, dhe `Scene` ne `Stage`. Layout panes kontrollojne si vendosen nodes.

### Pane kryesore

- `Pane`: baza; pozicionim manual me `layoutX/layoutY`.
- `FlowPane`: vendos elementet ne rresht dhe kalon ne rresht tjeter kur nuk ka vend.
- `GridPane`: ndan zonen ne rreshta dhe kolona.
- `BorderPane`: ndan hapesiren ne `top`, `bottom`, `left`, `right`, `center`.
- `StackPane`: vendos elementet mbi njeri-tjetrin, zakonisht ne qender.
- `HBox`: vendos elementet horizontalisht.
- `VBox`: vendos elementet vertikalisht.

### Shembull FlowPane

```java
FlowPane pane = new FlowPane();
pane.setHgap(10);
pane.setVgap(10);

pane.getChildren().addAll(
    new Label("First Name:"), new TextField(),
    new Label("Middle Initial:"), new TextField(),
    new Label("Last Name:"), new TextField()
);
```

### Shembull GridPane

```java
GridPane grid = new GridPane();
grid.setHgap(10);
grid.setVgap(10);

grid.add(new Label("Email:"), 0, 0);
grid.add(new TextField(), 1, 0);
grid.add(new Label("Password:"), 0, 1);
grid.add(new PasswordField(), 1, 1);
grid.add(new Button("Login"), 1, 2);
```

### Shembull BorderPane

```java
BorderPane root = new BorderPane();
root.setTop(new Label("Header"));
root.setLeft(new Button("Menu"));
root.setCenter(new TextArea());
root.setBottom(new Label("Status: gati"));
```

### Pika per provim

- Per forma perdor shpesh `GridPane`.
- Per strukture aplikacioni perdor `BorderPane`.
- Per lista vertikale perdor `VBox`; per toolbar horizontal perdor `HBox`.
- `getChildren().add(...)` shton nodes ne container.

---

## Ligjerata 8 - Shapes dhe figurat gjeometrike

### Shape

`Shape` eshte klase baze per forma gjeometrike. Format kane veti te perbashketa si:

- `fill`
- `stroke`
- `strokeWidth`
- koordinata
- madhesi
- transformime

### Line

`Line` percaktohet me dy pika: `startX`, `startY`, `endX`, `endY`.

```java
Line line = new Line(0, 0, 200, 300);
line.setStroke(Color.BLACK);
line.setStrokeWidth(3);
```

### Rectangle

`Rectangle` percaktohet nga pika e siperme e majte, gjeresia dhe lartesia.

```java
Rectangle rect = new Rectangle(50, 40, 180, 100);
rect.setFill(Color.LIGHTGREEN);
rect.setStroke(Color.DARKGREEN);
rect.setArcWidth(20);
rect.setArcHeight(20);
```

### Circle

```java
Circle circle = new Circle(150, 120, 60);
circle.setFill(Color.ORANGE);
circle.setStroke(Color.BROWN);
```

### Text vs Label

- `Text`: node grafike per shfaqje teksti, e pershtatshme kur trajtohet si pjese vizuale e skenes.
- `Label`: control UI, perdoret me forms dhe controls tjera.

Shembull i kombinuar:

```java
Pane pane = new Pane();

Text title = new Text(40, 50, "Forma ne JavaFX");
title.setStyle("-fx-font-size: 24px;");

Circle circle = new Circle(100, 140, 45);
circle.setFill(Color.SKYBLUE);

Rectangle rectangle = new Rectangle(180, 100, 120, 80);
rectangle.setFill(Color.LIGHTCORAL);

pane.getChildren().addAll(title, circle, rectangle);
```

### Pika per provim

- `Shape` ka `fill` dhe `stroke`.
- `Line` ka piken fillestare dhe perfundimtare.
- `Rectangle` ka `x`, `y`, `width`, `height`.
- `Circle` ka `centerX`, `centerY`, `radius`.

---

## Ligjerata 9 - Softueri i udhehequr nga ngjarjet

### Ideja kryesore

Ne GUI programi nuk ekzekutohet vetem rresht pas rreshti. Ai pret ngjarje: klikime, shtypje tastiere, levizje mouse, ndryshim fushe, mbyllje dritareje etj. Ky quhet softuer i udhehequr nga ngjarjet.

### Termat kryesore

- Event source: objekti ku ndodh ngjarja, p.sh. `Button`.
- Event object: objekti qe permban informacion per ngjarjen.
- Event handler: kodi qe ekzekutohet kur ndodh ngjarja.
- `EventHandler<T extends Event>`: interface qe implementohet nga handler-at.

### Shembull me klase te vecante

```java
import javafx.event.ActionEvent;
import javafx.event.EventHandler;
import javafx.scene.control.Label;

public class ClickHandler implements EventHandler<ActionEvent> {
    private final Label status;

    public ClickHandler(Label status) {
        this.status = status;
    }

    @Override
    public void handle(ActionEvent event) {
        status.setText("Butoni u klikua");
    }
}
```

Perdorimi:

```java
Button button = new Button("Kliko");
Label status = new Label("Duke pritur...");
button.setOnAction(new ClickHandler(status));
```

### Shembull i plote

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.control.Label;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;

public class EventExample extends Application {
    @Override
    public void start(Stage stage) {
        Label status = new Label("Duke pritur...");
        Button button = new Button("Kliko");

        button.setOnAction(event -> status.setText("U klikua!"));

        VBox root = new VBox(10, button, status);
        stage.setScene(new Scene(root, 300, 180));
        stage.show();
    }
}
```

### Pika per provim

- Event-driven do te thote programi reagon ndaj ngjarjeve.
- Butoni eshte burim ngjarjeje.
- Handler-i eshte kodi qe perpunon ngjarjen.
- `setOnAction(...)` perdoret shpesh per butona.

---

## Ligjerata 10 - Klasat e brendshme dhe handler-at anonim

### Klasat e brendshme

Klasat e brendshme perdoren kur nje klase ka kuptim vetem brenda nje klase tjeter. Ne JavaFX, perdoren shpesh per handler-a sepse handler-i ka nevoje te qase komponentet e GUI-se se jashtme.

```java
public class Outer {
    private int value = 10;

    class Inner {
        void printValue() {
            System.out.println(value);
        }
    }
}
```

### Handler si klase e brendshme

```java
public class InnerClassExample extends Application {
    private Label status = new Label("Gati");

    @Override
    public void start(Stage stage) {
        Button button = new Button("Ruaj");
        button.setOnAction(new SaveHandler());

        VBox root = new VBox(10, button, status);
        stage.setScene(new Scene(root, 300, 160));
        stage.show();
    }

    private class SaveHandler implements EventHandler<ActionEvent> {
        @Override
        public void handle(ActionEvent event) {
            status.setText("Te dhenat u ruajten");
        }
    }
}
```

### Klasa e brendshme anonime

Klasa anonime nuk ka emer dhe shkruhet aty ku krijohet objekti.

```java
button.setOnAction(new EventHandler<ActionEvent>() {
    @Override
    public void handle(ActionEvent event) {
        status.setText("Klikim nga handler anonim");
    }
});
```

Tipare nga materiali:

- Duhet t'i implementoje metodat abstrakte te interface/superclass.
- Kur implementon interface, konstruktori baze eshte `Object()`.
- Kompilohet me emer te tipit `OuterClassName$1.class`, `OuterClassName$2.class`.

### Lambda expression

Ne Java moderne, handler-at shpesh shkruhen me lambda:

```java
button.setOnAction(event -> status.setText("Klikim me lambda"));
```

Per provim mund te kerkohet forma klasike me `EventHandler`, prandaj dije te dyja.

---

## Ligjerata 11 - Paradigmat ne HCI

### Cfare jane paradigmat?

Paradigmat jane korniza teorike ose menyra dominuese e te menduarit per nje fushe. Ne HCI, paradigmat tregojne si ka ndryshuar marredhenia njeri-kompjuter gjate historise.

### Pse studiohen?

Materiali thekson dy pyetje:

- Si zhvillohet nje sistem interaktiv qe siguron perdorshmeri?
- Si mund te demonstrohet ose matet perdorimi i nje sistemi interaktiv?

Historia e teknologjive interaktive jep shembuj per dizajn te perdorshem.

### Zhvendosje historike

Paradigmat lidhen me zhvillimin e teknologjise:

- Llogaritjet e hershme kompjuterike: kompjuteri si makine llogaritese.
- Batch processing dhe kartelat me vrima: interaksion i ngadalte, feedback i vone.
- Time-sharing: me shume perdorues qasen ne sistem.
- Kompjuteri personal: perdoruesi ka kontroll direkt.
- GUI/WIMP: windows, icons, menus, pointer.
- Hypertext dhe web: lidhje, navigim, dokumente te nderlidhura.
- Ubiquitous/mobile computing: kompjuteri gjendet kudo.

### Pika per provim

- Paradigmat tregojne si ndryshon menyra e interaksionit.
- GUI dhe direct manipulation jane paradigma te rendesishme.
- Paradigmat nuk jane vetem teknologji; jane menyra te reja te mendimit per perdoruesin dhe detyren.

---

## Ligjerata 12 - Bazat e dizajnit te interaksionit

### Cfare eshte dizajni?

Materiali e pershkruan dizajnin si arritje te cakut brenda kufizimeve.

- Caku: per ke eshte dhe pse e duan.
- Kufizimet: materiale, platforma, kohe, kosto, teknologji, aftesi te perdoruesit.
- Kompromiset: zgjedhje midis alternativave qe nuk mund te jene te gjitha perfekte.

### Rregulla e arte

Rregulla e arte: kupto materialin tend. Ne HCI, materiali nuk eshte vetem kodi; materiali eshte edhe perdoruesi, pajisja, konteksti, detyra, koha dhe informacioni.

### Procesi i dizajnit

Procesi perfshin:

- Analiza: cfare duhet, kush jane perdoruesit, cfare pune kryejne.
- Dizajni: ide, strukture, navigim, dialog, prototip.
- Implementimi dhe shperndarja: realizimi teknik.
- Evaluimi: testim, rregulla, feedback nga perdoruesit.

Materiali permend intervista etnografike, analiza pune, prototipim, specifikim dhe evaluim.

### Dizajni i fokusuar te perdoruesi

Pyetje qe duhet bere:

- Kush jane perdoruesit?
- Cfare duan te arrijne?
- Cfare dine dhe cfare nuk dine?
- Ne cfare ambienti e perdorin sistemin?
- Cfare gabimesh mund te ndodhin?
- Cfare feedback-u u duhet?

### Shembull praktik

Nese dizajnon nje forme per regjistrim studenti:

- Mos kerko fusha te panevojshme.
- Vendos etiketa te qarta.
- Jep validim afer fushes.
- Ruaj gjendjen kur ndodh gabim.
- Perdor `required`, `placeholder`, dhe mesazhe gabimi te kuptueshme.
- Butoni kryesor duhet te tregoje qarte veprimin: `Regjistro`, jo `OK`.

### Pika per provim

- Dizajni eshte proces iterativ, jo vetem vizatim i nderfaqes.
- Perdoruesi duhet perfshire heret.
- Prototipi ndihmon para implementimit final.
- Evaluimi tregon nese dizajni punon realisht.

---

## Ligjerata 13 - HCI ne proceset e softuerit

### Modeli i ujvares

Modeli i ujvares ka faza te renditura:

1. Kerkesat softuerike
2. Dizajni i arkitektures
3. Dizajni detal
4. Kodimi dhe testimi njesi
5. Integrimi dhe testimi
6. Operimi dhe mirembajtja

Problemi per HCI eshte se nese perdoruesi perfshihet vone, gabimet e dizajnit zbulohen vone dhe jane me te shtrenjta per t'u rregulluar.

### Waterfall vs Agile

Waterfall:

- i strukturuar
- i planifikuar paraprakisht
- me faza te qarta
- me pak fleksibel ndaj ndryshimeve

Agile:

- fleksibel
- pranon ndryshime edhe pas planifikimit fillestar
- punon me iteracione
- mundeson feedback te shpejte

Materiali thekson se Agile eshte adoptuar gjeresisht sepse i pershtatet me mire ndryshimeve te kerkesave.

### Scrum

Nga materiali teorik:

- Product Owner ka vizion, autoritet dhe disponueshmeri.
- Ai komunikon vizionin dhe prioritetet me ekipin.
- Percakton vecorite e produktit.
- Duhet te jete i disponueshem per pyetje, por pa mikromenaxhuar ekipin.

Scrum zakonisht perfshin:

- Product Backlog
- Sprint Planning
- Sprint
- Daily Scrum
- Sprint Review
- Sprint Retrospective

### HCI brenda procesit

HCI duhet futur ne proces si:

- analiza e perdoruesve
- prototipim
- testim perdorshmerie
- iterim bazuar ne feedback
- matje e suksesit
- permiresim i vazhdueshem

### Pika per provim

- Waterfall eshte linear; Agile eshte iterativ.
- HCI preferon iterim dhe feedback te hershem.
- Product Owner ne Scrum eshte lidhja midis vizionit, prioriteteve dhe ekipit.
- Testimi i perdorshmerise nuk duhet lene vetem ne fund.

---

## Permbledhje nga ushtrimet dhe detyrat

### JavaFX si programim GUI

`Përmbledhje_Detyrash_KNK.pdf` e thekson qe aplikacionet GUI dallojne nga aplikacionet console sepse bazohen ne objekte vizuale dhe ngjarje. JavaFX API perdoret si framework objektor: krijon controls, panes, shapes, event handlers, scene dhe stage.

Programi minimal me buton:

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.stage.Stage;

public class Main extends Application {
    @Override
    public void start(Stage primaryStage) {
        Button btnOk = new Button("OK");
        Scene scene = new Scene(btnOk, 200, 250);

        primaryStage.setTitle("Programi i pare ne JavaFX");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
```

Version me `StackPane`, qe butoni te mos e mbuloje te gjithe skenen:

```java
StackPane pane = new StackPane();
Button btnOk = new Button("OK");
pane.getChildren().add(btnOk);

Scene scene = new Scene(pane, 200, 250);
primaryStage.setScene(scene);
primaryStage.show();
```

### Binding i njeanshem dhe dyanshem

Binding i njeanshem: target-i ndryshon kur ndryshon source.

```java
circle.centerXProperty().bind(pane.widthProperty().divide(2));
circle.centerYProperty().bind(pane.heightProperty().divide(2));
```

Binding dyanshem: te dyja vetite ndikojne njera-tjetren.

```java
TextField field = new TextField();
StringProperty username = new SimpleStringProperty();

field.textProperty().bindBidirectional(username);
```

Kjo eshte e dobishme kur UI dhe modeli duhet te jene gjithmone te sinkronizuar.

### Font dhe Alpha Channel

Ngjyrat ne JavaFX bazohen ne RGB plus alpha channel. Alpha tregon transparencen.

```java
Color semiTransparent = new Color(0.2, 0.4, 0.8, 0.5);
```

Font-i nuk eshte vetem emri, por kombinim i emrit, peshes, qendrimit dhe madhesise.

```java
Text title = new Text("KNK");
title.setFont(Font.font("Arial", FontWeight.BOLD, FontPosture.REGULAR, 28));
```

### ImageView: madhesi dhe rrotullim

```java
Image image = new Image("file:image/us.gif");

ImageView original = new ImageView(image);

ImageView resized = new ImageView(image);
resized.setFitWidth(100);
resized.setFitHeight(100);

ImageView rotated = new ImageView(image);
rotated.setRotate(90);

pane.getChildren().addAll(original, resized, rotated);
```

### Arc, Ellipse, Polygon dhe Polyline

Pervec `Line`, `Rectangle` dhe `Circle`, materiali praktik perdor edhe:

- `Ellipse`: si rreth, por ka `radiusX` dhe `radiusY`.
- `Arc`: pjese harku me lloje `OPEN`, `CHORD`, `ROUND`.
- `Polygon`: forme e mbyllur nga pika.
- `Polyline`: vije e hapur nga pika.

Shembull `Arc`:

```java
Arc openArc = new Arc(155, 75, 50, 50, 0, 60);
openArc.setFill(Color.WHITE);
openArc.setType(ArcType.OPEN);
openArc.setStroke(Color.RED);
```

Shembull `Polygon`:

```java
Polygon polygon = new Polygon();
polygon.setFill(null);
polygon.setStroke(Color.BLACK);

ObservableList<Double> points = polygon.getPoints();
double centerX = 150;
double centerY = 100;
double radius = 60;

for (int i = 0; i < 6; i++) {
    points.add(centerX + radius * Math.cos(2 * i * Math.PI / 6));
    points.add(centerY - radius * Math.sin(2 * i * Math.PI / 6));
}
```

### Figura te kustomizuara

Materiali tregon menyren:

1. Krijo klase qe zgjeron nje pane, p.sh. `Pane`, `StackPane`, `GridPane`.
2. Ruaj vetite e figures si fusha.
3. Krijo metode `draw()` qe pastron dhe rivizaton figuren.
4. Kur ndryshon `width`, `height`, ngjyra ose kend, thirr `draw()`.

Shembull i thjeshte:

```java
class CustomTarget extends Pane {
    private double size = 120;

    public CustomTarget() {
        draw();
    }

    public void setSize(double size) {
        this.size = size;
        draw();
    }

    private void draw() {
        getChildren().clear();

        Circle outer = new Circle(size / 2, size / 2, size / 2);
        outer.setFill(null);
        outer.setStroke(Color.BLACK);

        Circle inner = new Circle(size / 2, size / 2, size / 4);
        inner.setFill(Color.RED);

        getChildren().addAll(outer, inner);
    }
}
```

### Drejtkendeshi i kustomizuar me 4 pjese

Ideja e detyres: krijo nje drejtkendesh me kater pjese trekendeshe, secila me ngjyre te ndryshme.

```java
class FourPartRectangle extends Pane {
    private double w = 250;
    private double h = 180;

    public FourPartRectangle() {
        draw();
    }

    private void draw() {
        getChildren().clear();

        double x0 = 10, y0 = 10;
        double x1 = x0 + w, y1 = y0;
        double x2 = x1, y2 = y0 + h;
        double x3 = x0, y3 = y2;
        double x4 = x0 + w / 2, y4 = y0 + h / 2;

        Polygon p1 = new Polygon(x0, y0, x4, y4, x1, y1);
        Polygon p2 = new Polygon(x1, y1, x4, y4, x2, y2);
        Polygon p3 = new Polygon(x2, y2, x4, y4, x3, y3);
        Polygon p4 = new Polygon(x3, y3, x4, y4, x0, y0);

        p1.setFill(Color.color(Math.random(), Math.random(), Math.random(), 0.5));
        p2.setFill(Color.color(Math.random(), Math.random(), Math.random(), 0.5));
        p3.setFill(Color.color(Math.random(), Math.random(), Math.random(), 0.5));
        p4.setFill(Color.color(Math.random(), Math.random(), Math.random(), 0.5));

        getChildren().addAll(p1, p2, p3, p4);
    }
}
```

### Kombinimi i drejtkendeshave

Ideja: vizato disa drejtkendesha ne te njejten qender, secili i rrotulluar me nje kend.

```java
class RotatedRectangles extends Pane {
    public RotatedRectangles(int count, int rotateStep) {
        Group group = new Group();

        for (int i = 0; i < count; i++) {
            Rectangle r = new Rectangle(50, 50, 180, 120);
            r.setFill(null);
            r.setStroke(Color.color(Math.random(), Math.random(), Math.random()));
            r.setRotate(i * rotateStep);
            group.getChildren().add(r);
        }

        getChildren().add(group);
    }
}
```

### TextField qe nuk pranon numra

Nga `KNK-Ushtrime.pdf`: te krijohet nje `TextInput` qe nuk pranon vlera numerike `0-9`. Nje zgjidhje e paster eshte me `TextFormatter`.

```java
import javafx.scene.control.TextField;
import javafx.scene.control.TextFormatter;

public class NoDigitsTextField extends TextField {
    public NoDigitsTextField() {
        TextFormatter<String> formatter = new TextFormatter<>(change -> {
            String newText = change.getControlNewText();

            if (newText.matches(".*\\d.*")) {
                return null;
            }

            return change;
        });

        setTextFormatter(formatter);
    }
}
```

Perdorimi:

```java
NoDigitsTextField nameField = new NoDigitsTextField();
nameField.setPromptText("Shkruaj emrin");
```

### TextField qe pranon vetem numra

```java
TextField numberField = new TextField();
numberField.setTextFormatter(new TextFormatter<String>(change -> {
    String next = change.getControlNewText();
    return next.matches("\\d*") ? change : null;
}));
```

### Levizja e nje forme me butona

```java
Circle circle = new Circle(100, 100, 30);
Button right = new Button("Djathtas");
Button left = new Button("Majtas");

right.setOnAction(e -> circle.setCenterX(circle.getCenterX() + 10));
left.setOnAction(e -> circle.setCenterX(circle.getCenterX() - 10));
```

### Ndryshimi i ngjyres me event

```java
Rectangle rect = new Rectangle(120, 80, Color.LIGHTGRAY);

rect.setOnMouseClicked(event -> {
    rect.setFill(Color.CORNFLOWERBLUE);
});
```

### Mapper, DTO, Repository - nga kodi praktik

Ne materialet e ushtrimeve/projekteve shfaqen edhe modele si `Student`, `StudentDto`, `StudentMapper`, `Repository`, `Service`. Ideja eshte ndarja e pergjegjesive:

- Model: objekti real/domain, p.sh. `Student`.
- DTO: objekt per transferim te te dhenave, p.sh. `StudentRequestDto`.
- Mapper: kthen modelin ne DTO ose DTO ne model.
- Repository: komunikon me bazen e te dhenave.
- Service: mban logjiken e biznesit.
- Controller: lidh UI me service.

Shembull i thjeshte:

```java
class Student {
    private int id;
    private String name;

    public Student(int id, String name) {
        this.id = id;
        this.name = name;
    }

    public int getId() {
        return id;
    }

    public String getName() {
        return name;
    }
}

record StudentDto(int id, String name) {}

class StudentMapper {
    public StudentDto toDto(Student student) {
        return new StudentDto(student.getId(), student.getName());
    }
}
```

### JDBC - lidhja me bazen e te dhenave

Materiali praktik ka kapitull per lidhjen e objekteve me bazen e te dhenave. JDBC eshte API qe lejon Java te komunikoje me DB.

Hapat kryesore:

1. Regjistrimi i driver-it.
2. Krijimi i lidhjes.
3. Krijimi i `Statement` ose `PreparedStatement`.
4. Ekzekutimi i SQL.
5. Leximi i `ResultSet`.
6. Mbyllja e lidhjes.

```java
public Connection getConnection() {
    try {
        return DriverManager.getConnection(
            "jdbc:mysql://localhost:3306/testdatabase",
            "root",
            "root"
        );
    } catch (SQLException e) {
        System.err.println(e.getMessage());
        return null;
    }
}
```

`Statement` perdoret per SQL statik. `PreparedStatement` eshte me i mire kur ka parametra dhe ndihmon kunder SQL injection.

```java
String sql = "SELECT * FROM users WHERE age > ?";
PreparedStatement ps = connection.prepareStatement(sql);
ps.setInt(1, 18);

ResultSet rs = ps.executeQuery();
while (rs.next()) {
    System.out.println(rs.getString("username"));
}
```

### DBConnect

`DBConnect` eshte klase ndihmese qe centralizon lidhjen dhe ekzekutimin e query-ve.

```java
class DBConnect {
    private static final String URL = "jdbc:mysql://localhost:3306/DBSTUDENTI";
    private static final String USER = "root";
    private static final String PASSWORD = "admin123";

    private Connection conn;

    private DBConnect() throws SQLException {
        conn = DriverManager.getConnection(URL, USER, PASSWORD);
    }

    public static DBConnect getInstance() throws SQLException {
        return new DBConnect();
    }

    public ResultSet executeQuery(String query, Object... values) throws SQLException {
        PreparedStatement ps = conn.prepareStatement(query);
        for (int i = 0; i < values.length; i++) {
            ps.setObject(i + 1, values[i]);
        }
        return ps.executeQuery();
    }
}
```

### QueryBuilder

Materiali permend `InsertQueryBuilder`, `UpdateQueryBuilder` dhe `FilterQueryBuilder`. Qellimi eshte gjenerimi i SQL ne menyre me te organizuar.

- `InsertQueryBuilder`: krijon `INSERT INTO ...`.
- `UpdateQueryBuilder`: krijon `UPDATE ... SET ... WHERE ...`.
- `FilterQueryBuilder`: krijon `SELECT * FROM ... WHERE ...`.

Shembull ideje:

```java
String query = "INSERT INTO students (name, age) VALUES (?, ?)";
Object[] values = {"Arta", 21};
```

Me QueryBuilder, keto pjese ndertohen nga metoda `add(...)` dhe `addWhere(...)`, pastaj merren `getQuery()`, `getTypes()` dhe `getValues()`.

### FXML dhe Controller

Ne projektin praktik, UI mund te ndahet ne fajlla FXML dhe logjike controller.

FXML:

```xml
<VBox xmlns:fx="http://javafx.com/fxml"
      fx:controller="controllers.LoginViewController">
    <children>
        <TextField fx:id="txtUsername" />
        <PasswordField fx:id="pwdPassword" />
        <Button text="Login" onAction="#loginEventHandler" />
    </children>
</VBox>
```

Controller:

```java
public class LoginViewController {
    @FXML
    private TextField txtUsername;

    @FXML
    private PasswordField pwdPassword;

    @FXML
    private void loginEventHandler(ActionEvent event) {
        String username = txtUsername.getText();
        String password = pwdPassword.getText();
        System.out.println(username + " " + password);
    }
}
```

Kalimi nga nje faqe ne tjetren:

```java
private void loadHomePage(Node source) throws IOException {
    FXMLLoader loader = new FXMLLoader(getClass().getResource("/views/HomeView.fxml"));
    Parent pane = loader.load();
    Scene scene = new Scene(pane, 640, 400);

    Stage stage = (Stage) source.getScene().getWindow();
    stage.setScene(scene);
}
```

### Struktura e projektit FiekNotimi

Materiali praktik propozon strukture te ndare:

- `application`: pjesa filluese, `main`.
- `controllers`: logjika e UI.
- `database`: lidhja me DB dhe query builders.
- `models`: klasat qe perfaqesojne tabela/rekorde.
- `DTO`: objekte per transferim te te dhenave.
- `processors` ose `services`: logjika e perpunimit.
- `repositories`: qasje ne DB per modele.
- `resources`: FXML, gjuhe, imazhe dhe fajlla ndihmes.
- `utilities`: klasa ndihmese.

Parim i rendesishem: controller-i nuk duhet te mbaje gjithe logjiken e biznesit. Ai duhet te lexoje UI dhe te therrase processor/service.

### I18N - perkthimi i aplikacionit

Materiali perdor klase `I18N` per lidhje dinamike te teksteve me gjuhen aktive.

```java
primaryStage.titleProperty().bind(
    I18N.createStringBinding("window.login.title")
);
```

Ideja: tekstet ruhen ne resource bundles, dhe UI merr tekstin me celes. Kur ndryshon locale, tekstet mund te rifreskohen.

### Login dhe SignUp

`LoginViewController` trajton eventet e login, cancel dhe reset password. `SignUpViewController` lexon fushat si emri, mbiemri, email, password dhe confirm password, krijon DTO dhe ia jep processor-it.

Shembull DTO:

```java
public record CreateUserDTO(
    String firstName,
    String lastName,
    String email,
    String password
) {}
```

Shembull processor:

```java
class SignUpProcessor {
    private final LoginRepository repository = new LoginRepository();

    public boolean createNewUser(CreateUserDTO userDto) {
        if (userDto.password().length() < 8) {
            return false;
        }

        return repository.create(userDto);
    }
}
```

### Repository per Student

Repository fsheh detajet e SQL nga pjesa tjeter e programit.

```java
class StudentRepository {
    private final Connection connection;

    StudentRepository(Connection connection) {
        this.connection = connection;
    }

    public Student findById(int id) throws SQLException {
        String sql = "SELECT * FROM students WHERE id = ?";
        PreparedStatement ps = connection.prepareStatement(sql);
        ps.setInt(1, id);

        ResultSet rs = ps.executeQuery();
        if (rs.next()) {
            return new Student(rs.getInt("id"), rs.getString("name"));
        }

        return null;
    }
}
```

---

## Pyetje te mundshme per provim

### Teori

1. Cfare eshte HCI/KNK dhe pse eshte e rendesishme?
2. Shpjego dallimin midis marrjes fizike te stimulit dhe interpretimit te tij.
3. Cilat jane tri llojet e memories dhe pse memoria afatshkurter eshte e rendesishme ne GUI?
4. Shpjego modelin e Norman-it me shtate faza.
5. Cfare jane hendeku i ekzekutimit dhe hendeku i vleresimit?
6. Cilat jane stilet kryesore te interaksionit?
7. Cfare jane paradigmat ne HCI?
8. Shpjego dizajnin e fokusuar te perdoruesi.
9. Krahaso Waterfall dhe Agile.
10. Cili eshte roli i Product Owner ne Scrum?

### JavaFX

1. Shpjego `Stage`, `Scene`, `Pane`, `Node`.
2. Shkruaj nje program minimal JavaFX.
3. Cfare eshte property binding?
4. Si stilizohet nje element me CSS ne JavaFX?
5. Dallimi midis `Text` dhe `Label`.
6. Si perdoret `ImageView`?
7. Krahaso `FlowPane`, `GridPane`, `BorderPane`.
8. Shpjego `Shape`, `Line`, `Rectangle`, `Circle`.
9. Cfare eshte event-driven programming?
10. Shkruaj handler me klase te brendshme, klase anonime dhe lambda.

---

## Mini-cheatsheet JavaFX

```java
// Stage + Scene
stage.setScene(new Scene(root, 400, 300));
stage.show();

// Shto node ne pane
pane.getChildren().add(button);

// Event
button.setOnAction(event -> System.out.println("Clicked"));

// CSS inline
button.setStyle("-fx-background-color: blue; -fx-text-fill: white;");

// Binding
circle.centerXProperty().bind(pane.widthProperty().divide(2));

// Shape
Circle c = new Circle(100, 100, 40);
c.setFill(Color.RED);

// Image
ImageView view = new ImageView(new Image("file:image.png"));
view.setFitWidth(200);
view.setPreserveRatio(true);
```

---

## Si ta mesosh shpejt

1. Lexo ligjeratat 1-3 per bazen teorike te HCI.
2. Mesoi permendsh termat: perceptim, memorie, model i Norman-it, hendek ekzekutimi/vleresimi, paradigma.
3. Pastaj ushtro JavaFX nga ligjeratat 4-10: nje program minimal, panelet, shapes, event handlers.
4. Ne fund lexo ligjeratat 11-13 per paradigmat, dizajnin dhe proceset softuerike.
5. Per cdo pyetje praktike, shkruaj kod me strukturen: `Application`, `start`, `Pane`, `Scene`, `Stage`, `event handler`.
