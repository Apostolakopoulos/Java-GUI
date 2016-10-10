# Gui
Graphical Users Interface

    import javax.swing.JOptionPane; //Eisagwgh bibliothikhs
    public class apples {
      public static void main(String args[]){
        String fn = JOptionPane.showInputDialog("Enter first number : ");//emfanizei parathiro eisagwghs kai oti balei ekei o xrhsths
        String sn = JOptionPane.showInputDialog("Enter second number : ");//mpainei sthn fn kai sthn sn antistoixa

        int num1 = Integer.parseInt(fn);//metatrepei se int auto pou dinei o xrhsths
        int num2 = Integer.parseInt(sn);
        int sum = num1 + num2;
        JOptionPane.showMessageDialog(null, "The answer is : "+sum ,"First Message", JOptionPane.PLAIN_MESSAGE);
        //emfanizei to apotelesma 
      } 
    }
