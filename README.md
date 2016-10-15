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
#Event Handler Program

    import javax.swing.JFrame;
    public class apples {
        public static void main(String args[]){		
            tuna stef = new tuna();//object tuna
            stef.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);//kleinei to parathhro
            stef.setSize(350, 100);//ftiaxnw to size
            stef.setVisible(true);//to kanw emfanes
        } 
    }
    
    import java.awt.FlowLayout;
    import java.awt.event.ActionListener;//perimenei an kanei kati o xrhsths
    import java.awt.event.ActionEvent;
    import javax.swing.JFrame;
    import javax.swing.JTextField;//dinei ta textfields
    import javax.swing.JPasswordField;//dinei ta JpasswordFields
    import javax.swing.JOptionPane;
    
    public class  tuna extends JFrame{//ftiaxnoume parathhro
        private JTextField item1;//Dhmiourgw 3 metablhtes JTextField
        private JTextField item2;
        private JTextField item3;
        private JPasswordField pass;//typou JPasswordField	

        public tuna(){//Dhmiourgeia constructor kai aparthhrou
            super ( "Τιτλος Παραθύρου");
            setLayout(new FlowLayout());
            item1 =new JTextField(10);//dhmiourgei JTextField object me parametrous
            add(item1);//eisagwgh item1 field
            item2 =new JTextField("Enter text Here:");//dhmiourgei JTextField object me parametrous
            add(item2);// eisagwgh item2 field
            item3 = new JTextField("oti thelw", 20);//dhmiourgei JTextField object me parametrous
            item3.setEditable(false);//gia na mhn m porei na kanei edit
            add(item3);// eisagwgh item3 field
            pass = new JPasswordField("My pass");//dhmiourgei JPassword object
            add(pass);// eisagwgh pass	

            thehandler handler = new thehandler();//dhmiourgeia object
            item1.addActionListener(handler);//topothetoume sthn item1 ton actionListener
            item2.addActionListener(handler);
            item3.addActionListener(handler);
            pass.addActionListener(handler);
        }	

        private class thehandler implements ActionListener{//dhmiourgeia klashw gia action Listener
            public void actionPerformed(ActionEvent event){//dhmiourgeia methodou
                String string = "" ;
                if (event.getSource() == item1 ){//h phgh h opoia pairnei to event pou einai to action 1 				
                    string=String.format("Field1: %s", event.getActionCommand());//
                }else if(event.getSource() == item2){
                    string=String.format("Field2: %s", event.getActionCommand());
                }else if(event.getSource() == item3){
                    string=String.format("Field3: %s", event.getActionCommand());
                }else if(event.getSource() == pass){
                    string=String.format("The password field is:  %s", event.getActionCommand());
                }
                JOptionPane.showConfirmDialog(null, string);//null gia th thesh kai string ti tha bgalei
            }
        }
    }

