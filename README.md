import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
public class Main{
    public static void main(String[] args)
    {
        JFrame frame = new JFrame("Simple GUI");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setSize(300,200);
        
        JTextField textField = new JTextField();
        textField.setBounds(50, 50, 200, 30);
        JButton button = new JButton("click Me");
        button.setBounds(100, 100, 100, 30);
        
        button.addActionListener(new ActionListener(){
             public void actionPerformed(ActionEvent e) {
                String input = textField.getText();
                JOptionPane.showMessageDialog(frame, "You entered: " + input);
            }
        });
        frame.add(textField);
        frame.setVisible(true);
        
    }
}
