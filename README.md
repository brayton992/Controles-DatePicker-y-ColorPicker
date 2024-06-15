## EXPLICACION DEL CODIGO

Este código JavaFX proporciona una interfaz simple donde los usuarios pueden seleccionar una fecha y un color, y ver esas selecciones impresas en la consola. Utiliza controles estándar de JavaFX como DatePicker, ColorPicker, Label, y Button, organizados dentro de un layout VBox. La acción del botón captura las selecciones y las imprime, mostrando cómo interactuar con los componentes de JavaFX.

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.*;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;
import javafx.geometry.Insets;
import javafx.scene.paint.Color;

public class DatePickerColorPickerExample extends Application {

    @Override
    public void start(Stage primaryStage) {
        // Crear los controles
        Label dateLabel = new Label("Selecciona una fecha:");
        DatePicker datePicker = new DatePicker();

        Label colorLabel = new Label("Selecciona un color:");
        ColorPicker colorPicker = new ColorPicker();

        Button submitButton = new Button("Confirmar");

        // Acción del botón
        submitButton.setOnAction(e -> {
            // Obtener la fecha y el color seleccionados
            String selectedDate = datePicker.getValue().toString();
            Color selectedColor = colorPicker.getValue();

            // Mostrar en consola
            System.out.println("Fecha seleccionada: " + selectedDate);
            System.out.println("Color seleccionado: " + selectedColor);
        });

        // Crear el layout y añadir los controles
        VBox vbox = new VBox(10);
        vbox.setPadding(new Insets(20));
        vbox.getChildren().addAll(dateLabel, datePicker, colorLabel, colorPicker, submitButton);

        // Crear la escena
        Scene scene = new Scene(vbox, 300, 250);

        // Configurar el escenario (Stage)
        primaryStage.setTitle("Ejemplo de DatePicker y ColorPicker en JavaFX");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
```

   
## Practica de interface 

## Imagen de ejemplo de la tarea
![image](https://github.com/brayton992/Controles-DatePicker-y-ColorPicker/assets/142423609/23192284-6e0b-4402-8bbf-7d38842b37f5)


## DatePicker

 Un control de selección de fecha que permite a los usuarios seleccionar una fecha específica desde un calendario desplegable. Este componente facilita la entrada de datos de fecha, mejorando la precisión y la usabilidad al evitar errores de formato.

## ColorPicker

Un control de selección de color que permite a los usuarios elegir un color específico desde una paleta de colores. Este componente suele incluir una gama de colores y, a veces, opciones avanzadas como la selección de tonos y matices, proporcionando una forma intuitiva de seleccionar colores.

## Button

Un botón interactivo que permite a los usuarios confirmar la selección de la fecha y el color. Al presionar este botón, se ejecuta una acción que puede procesar, guardar o mostrar las selecciones realizadas por el usuario.

## Label

Etiquetas de texto que proporcionan instrucciones y guías a los usuarios sobre las acciones que deben realizar. Por ejemplo, etiquetas como "Selecciona una fecha:" y "Selecciona un color:" orientan al usuario y mejoran la claridad de la interfaz.

## VBox Layout

Un layout vertical (VBox) que organiza los controles de manera ordenada y clara en una columna. Utilizar VBox facilita la alineación y distribución de los componentes en la interfaz, proporcionando una apariencia limpia y estructurada.


## Acción al Presionar el Botón

La funcionalidad que se activa al presionar el botón, donde la fecha y el color seleccionados se muestran en la consola o en otro componente de la interfaz. Esta acción puede incluir la validación de las selecciones y su presentación en un formato legible, mejorando la interactividad y la retroalimentación del sistema al usuario.
