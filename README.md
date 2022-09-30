CANVAS GENERATE SKY AND SUN

En esta practica se realizo la actividad de dibujar el cielo con un sol, primero se creo un ventana para en el añadir objetos y sus caracteristicas en este caso un rectangulo de color gris y otro rectangulo de color azul cielo y posteriormente se añadio un circulo amarillo representativo del sol. Se me hace interesante este tipo de actividades.

![image](https://user-images.githubusercontent.com/112669364/192937933-435aab69-bb39-4a2b-a9de-e70e3fcdcfdc.png)

//CODIGO PARA GENERERAR LA VENTANA Y AÑADIR LOS ELEMENTOS 

import javax.swing.*;
 
class Swing01 {
   public static void main (String args[]){
       JFrame window = new JFrame("Swing");
       MyCanvas canvas = new MyCanvas();
 
       window.setDefaultCloseOperation(WindowConstants.EXIT_ON_CLOSE);
       window.setSize(400, 300);
       window.add(canvas);
       window.pack();
       window.setResizable(false);
       window.setLocationRelativeTo(null);
       window.setVisible(true);
   }
}

//CODIGO PARA PINTAR LOS OBJETOS

import java.awt.Color;
import java.awt.Dimension;
import javax.swing.JPanel;
import java.awt.Graphics;
 
public class MyCanvas extends JPanel {
   public MyCanvas () {
       setPreferredSize(new Dimension(400,300));
       setBackground(Color.GRAY);
   }
   @Override
   protected void paintComponent(Graphics g){
       super.paintComponent(g);

       g.setColor(new Color (127,233,245));
       g.fillRect(0,0, 400, 100);
 
       g.setColor(Color.YELLOW);
       g.fillOval(40, 40, 20, 20);
   }
}
