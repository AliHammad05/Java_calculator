import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JButton;
import javax.swing.JTextField;
import javax.swing.JLabel;
import javax.swing.JOptionPane;

import java.awt.Font;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
import javax.swing.JPopupMenu;

public class Calculator_ass {

	private JFrame frame;
	private JTextField textField01;
	private JTextField textField02;
	private JTextField textField03;
	private JLabel lblNewLabel;
	private JButton ButtonSum;
	private JButton ButtonSub;
	private JButton ButtonMul;
	private JButton ButtonDev;
	private JLabel lblFirstValue;
	private JLabel lblSecondValue;
	private JLabel lblNewLabel_2;
	/**
	 * @wbp.nonvisual location=551,184
	 */
	private final JPopupMenu popupMenu = new JPopupMenu();

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					Calculator_ass window = new Calculator_ass();
					window.frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the application.
	 */
	public Calculator_ass() {
		initialize();
	}

	/**
	 * Initialize the contents of the frame.
	 */
	private void initialize() {
		frame = new JFrame();
		frame.setBounds(100, 100, 435, 375);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.getContentPane().setLayout(null);
		
		textField01 = new JTextField();
		textField01.setBounds(21, 105, 164, 45);
		frame.getContentPane().add(textField01);
		textField01.setColumns(10);
		
		textField02 = new JTextField();
		textField02.setBounds(231, 105, 164, 45);
		frame.getContentPane().add(textField02);
		textField02.setColumns(10);
		
		textField03 = new JTextField();
		textField03.setBounds(166, 231, 164, 45);
		frame.getContentPane().add(textField03);
		textField03.setColumns(10);
		
		lblNewLabel = new JLabel("ANS");
		lblNewLabel.setFont(new Font("Tahoma", Font.BOLD, 16));
		lblNewLabel.setBounds(100, 245, 45, 13);
		frame.getContentPane().add(lblNewLabel);
		
		ButtonSum = new JButton("+");
		ButtonSum.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				try {
					int num1,num2,ans;
					num1=Integer.parseInt(textField01.getText());
					num2=Integer.parseInt(textField02.getText());
					
					ans=num1+num2;
					textField03.setText(Integer.toString(ans));
				}
				catch(Exception e1) {
					JOptionPane.showMessageDialog(null, "Enter Valid Num ");
				}
				
			}
		});
		ButtonSum.setFont(new Font("Tahoma", Font.PLAIN, 20));
		ButtonSum.setBounds(21, 176, 76, 45);
		frame.getContentPane().add(ButtonSum);
		
		ButtonSub = new JButton("-");
		ButtonSub.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				try {
					int num1,num2,ans;
					num1=Integer.parseInt(textField01.getText());
					num2=Integer.parseInt(textField02.getText());
					
					ans=num1-num2;
					textField03.setText(Integer.toString(ans));
				}
				catch(Exception e1) {
					JOptionPane.showMessageDialog(null, "Enter Valid Num ");
				}
			}
		});
		ButtonSub.setFont(new Font("Tahoma", Font.PLAIN, 20));
		ButtonSub.setBounds(107, 176, 76, 45);
		frame.getContentPane().add(ButtonSub);
		
		ButtonMul = new JButton("x");
		ButtonMul.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				try {
					int num1,num2,ans;
					num1=Integer.parseInt(textField01.getText());
					num2=Integer.parseInt(textField02.getText());
					
					ans=num1*num2;
					textField03.setText(Integer.toString(ans));
				}
				catch(Exception e1) {
					JOptionPane.showMessageDialog(null, "Enter Valid Num ");
				}
			}
		});
		ButtonMul.setFont(new Font("Tahoma", Font.PLAIN, 20));
		ButtonMul.setBounds(231, 176, 76, 45);
		frame.getContentPane().add(ButtonMul);
		
		ButtonDev = new JButton("/");
		ButtonDev.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				try {
					int num1,num2,ans;
					num1=Integer.parseInt(textField01.getText());
					num2=Integer.parseInt(textField02.getText());
					
					ans=num1/num2;
					textField03.setText(Integer.toString(ans));
				}
				catch(Exception e1) {
					JOptionPane.showMessageDialog(null, "Enter Valid Num ");
				}
			}
		});
		ButtonDev.setFont(new Font("Tahoma", Font.PLAIN, 20));
		ButtonDev.setBounds(319, 176, 76, 45);
		frame.getContentPane().add(ButtonDev);
		
		lblFirstValue = new JLabel("First Value");
		lblFirstValue.setFont(new Font("Tahoma", Font.BOLD, 16));
		lblFirstValue.setBounds(55, 82, 106, 13);
		frame.getContentPane().add(lblFirstValue);
		
		lblSecondValue = new JLabel("Second Value");
		lblSecondValue.setFont(new Font("Tahoma", Font.BOLD, 16));
		lblSecondValue.setBounds(257, 82, 121, 13);
		frame.getContentPane().add(lblSecondValue);
		
		JLabel lblNewLabel_1 = new JLabel("Calculator");
		lblNewLabel_1.setFont(new Font("Tahoma", Font.BOLD, 28));
		lblNewLabel_1.setBounds(134, 23, 153, 34);
		frame.getContentPane().add(lblNewLabel_1);
		
		lblNewLabel_2 = new JLabel("Designed By M Ali Hammad(4982)");
		lblNewLabel_2.setFont(new Font("Tahoma", Font.BOLD, 20));
		lblNewLabel_2.setBounds(34, 286, 361, 42);
		frame.getContentPane().add(lblNewLabel_2);
	}
}
