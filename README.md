package assi;

import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JOptionPane;
import javax.swing.JTextField;
import javax.swing.JButton;
import java.awt.Font;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;
import javax.swing.JLabel;

public class assi {

	private JFrame frame;
	private JTextField textField01;
	private JTextField textField02;
	private JTextField textField03;

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					assi window = new assi();
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
	public assi() {
		initialize();
	}

	/**
	 * Initialize the contents of the frame.
	 */
	private void initialize() {
		frame = new JFrame();
		frame.setBounds(100, 100, 450, 453);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.getContentPane().setLayout(null);
		
		textField01 = new JTextField();
		textField01.setBounds(57, 40, 324, 69);
		frame.getContentPane().add(textField01);
		textField01.setColumns(10);
		
		textField02 = new JTextField();
		textField02.setColumns(10);
		textField02.setBounds(57, 194, 324, 69);
		frame.getContentPane().add(textField02);
		
		textField03 = new JTextField();
		textField03.setColumns(10);
		textField03.setBounds(57, 290, 324, 69);
		frame.getContentPane().add(textField03);
		
		JButton btnNewButtonsum = new JButton("+");
		btnNewButtonsum.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				try {
					int num1,num2,ans;
					num1=Integer.parseInt(textField01.getText());
					num2=Integer.parseInt(textField02.getText());
					ans=num1+num2;
					textField03.setText(Integer.toString(ans));
				}
				catch(Exception e1) 
				{
					JOptionPane.showMessageDialog(null,"Enter valid Numver");
				}
			}
		});
		btnNewButtonsum.setFont(new Font("Tahoma", Font.BOLD, 20));
		btnNewButtonsum.setBounds(67, 130, 71, 48);
		frame.getContentPane().add(btnNewButtonsum);
		
		JButton btnNewButtonsub = new JButton("-");
		btnNewButtonsub.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				try {
					int num1,num2,ans;
					num1=Integer.parseInt(textField01.getText());
					num2=Integer.parseInt(textField02.getText());
					ans=num1-num2;
					textField03.setText(Integer.toString(ans));
				}
				catch(Exception e1) 
				{
					JOptionPane.showMessageDialog(null,"Enter valid Numver");
				}
			}
		});
		btnNewButtonsub.setFont(new Font("Tahoma", Font.BOLD, 20));
		btnNewButtonsub.setBounds(148, 130, 71, 48);
		frame.getContentPane().add(btnNewButtonsub);
		
		JButton btnNewButtonmul = new JButton("x");
		btnNewButtonmul.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				try {
					int num1,num2,ans;
					num1=Integer.parseInt(textField01.getText());
					num2=Integer.parseInt(textField02.getText());
					ans=num1*num2;
					textField03.setText(Integer.toString(ans));
				}
				catch(Exception e1) 
				{
					JOptionPane.showMessageDialog(null,"Enter valid Numver");
				}
			}
		});
		btnNewButtonmul.setFont(new Font("Tahoma", Font.BOLD, 20));
		btnNewButtonmul.setBounds(229, 130, 71, 48);
		frame.getContentPane().add(btnNewButtonmul);
		
		JButton btnNewButtondiv = new JButton("/");
		btnNewButtondiv.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) {
				
				try {
					int num1,num2,ans;
					num1=Integer.parseInt(textField01.getText());
					num2=Integer.parseInt(textField02.getText());
					ans=num1/num2;
					textField03.setText(Integer.toString(ans));
				}
				catch(Exception e1) 
				{
					JOptionPane.showMessageDialog(null,"Enter valid Numver");
				}
			}
		});
		btnNewButtondiv.setFont(new Font("Tahoma", Font.BOLD, 20));
		btnNewButtondiv.setBounds(310, 130, 71, 48);
		frame.getContentPane().add(btnNewButtondiv);
		
		JLabel lblNewLabel = new JLabel("Designed By Mujeeb Ur Rehman (4646)");
		lblNewLabel.setFont(new Font("Tahoma", Font.BOLD, 16));
		lblNewLabel.setBounds(67, 376, 324, 27);
		frame.getContentPane().add(lblNewLabel);
	}
}
