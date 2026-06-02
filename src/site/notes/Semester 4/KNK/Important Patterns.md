---
{"dg-publish":true,"permalink":"/semester-4/knk/important-patterns/"}
---

# Important KNK JavaFX patterns  
  
## Stage, Scene, Pane  
  
```java  
Pane root = new Pane();  
Scene scene = new Scene(root, 500, 350);  
stage.setScene(scene);  
stage.show();  
```  
  
## Add nodes  
  
```java  
pane.getChildren().add(node);  
pane.getChildren().addAll(node1, node2, node3);  
```  
  
## Event handler  
  
```java  
button.setOnAction(event -> label.setText("Clicked"));  
```  
  
## Timeline animation  
  
```java  
KeyFrame frame = new KeyFrame(Duration.millis(16), event -> {  
    circle.setCenterX(circle.getCenterX() + 2);});  
Timeline timeline = new Timeline(frame);  
timeline.setCycleCount(Animation.INDEFINITE);  
timeline.play();  
```  
  
## Binding  
  
```java  
circle.centerXProperty().bind(pane.widthProperty().divide(2));  
circle.centerYProperty().bind(pane.heightProperty().divide(2));  
```  
  
## TextFormatter  
  
```java  
field.setTextFormatter(new TextFormatter<String>(change ->  
    change.getControlNewText().matches("\\d*") ? change : null));  
```  
  
## Custom shape  
  
```java  
class MyShape extends Pane {  
    private void draw() {        getChildren().clear();        getChildren().add(new Circle(50, 50, 40));    }}  
```  
  
## PreparedStatement  
  
```java  
PreparedStatement ps = connection.prepareStatement("SELECT * FROM students WHERE id = ?");  
ps.setInt(1, id);  
ResultSet rs = ps.executeQuery();  
```  
  
## DTO, mapper, repository  
  
- DTO transfers data.  
- Mapper converts `ResultSet` or model objects.  
- Repository hides SQL.  
- Service/processor contains business logic.  
- Controller connects UI with service.