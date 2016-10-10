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
# Gui with JFrame 
    import javax.swing.JFrame;
    public class apples {
        public static void main(String args[]){
            tuna object = new tuna();//antikeimeno ths klashs tuna
            object.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);//dhlwsh pws na kleinei... otana patame to X gia kleishmo
            object.setSize(400,400);//ftiaxnw to megethos platos, upsos
            object.setVisible(true);//emfanizetai kai oxi sto paraskhnio
        } 
    }
    import java.awt.FlowLayout;  //Sxediagramma rohs
    import javax.swing.JFrame;  //Basiko dunatothtes Whindow
    import javax.swing.JLabel; //eisagwgh label
    public class  tuna extends JFrame{	//klhrwnomei apo th JFrame class oles tis methodous
        private JLabel item1; //tupos JLabel
        public tuna(){
            super ("Προγραμμα Εμφάνισης Πρότασης"); //eisagwgh titlou sto parathuro
            setLayout(new FlowLayout()); //dinei to default layout	
            item1 = new JLabel("Εμφανίζεται αυτό το κείμενο μέσα στο πρόγραμμα ");
            item1.setToolTipText("Οταν βάζω τον δείκτη από επάνω εμφανίζεται αυτό ");
            add(item1);//eisagei to item
        }
    }
