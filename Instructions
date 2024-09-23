/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Main.java to edit this template
 */
package teststrategy;
/**
 *
 * @author MSI
 */
public class TestStrategy {
    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Cart cart = new Cart(1512.75);
        cart.pay(new Online("mark.reyes@gmail.com", "Wasd8456!")); 
        
        cart = new Cart(375.25);
        cart.pay(new Mobile("12105733109", 627326));
    }    
}

interface Payment{    
    public void pay(double amount);
}

class Online implements Payment{
    private String email;
    private String password;
    
    public Online(String email, String password){
        this.email = email;
        this.password = password;
    }
    @Override
    public void pay(double amount) {
        System.out.println("Paid using online account: " + amount);
    }
}

class Mobile implements Payment{
    private String number;
    private int pin;
    
    public Mobile(String number, int pin){
        this.number = number;
        this.pin = pin;
    }
    @Override
    public void pay(double amount) {
        System.out.println("Paid using mobile wallet: " + amount);
    }
}

class Cart{
    private double amount;
    public Cart(double amount){
        this.amount = amount;
    }
    public void pay(Payment mode){
        mode.pay(amount);
    }
}
