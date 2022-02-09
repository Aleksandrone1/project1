# project1
package sample;

import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Alert;
import javafx.scene.control.Button;
import javafx.scene.layout.FlowPane;
import javafx.stage.Stage;

public class Main extends Application {
    public void start(Stage stage) {

        Button button=new Button("кнопка 1");//создание кнопки
        button.setOnAction(event-> {
            Alert alert = new Alert(Alert.AlertType.INFORMATION);// создание диалогового окна
            alert.setTitle("Окно");
            alert.setContentText("Мой первый проект на github");

            alert.showAndWait();
        });
        FlowPane root = new FlowPane(button);       // корневой узел
        Scene scene = new Scene(root, 300, 150);        // создание Scene
        stage.setScene(scene);                          // установка Scene для Stage

        stage.setTitle("Hello JavaFX");// название окна

        stage.show();
    }
    public static void main(String[] args) {
        launch(args);
    }

}
