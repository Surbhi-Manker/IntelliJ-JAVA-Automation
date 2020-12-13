# IntelliJ-JAVA-Automation
Selenium-Java- Scripts


package com.google;
import org.openqa.selenium.By;

import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.firefox.FirefoxDriver;

import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
       {
        System.out.println("Hello");
       }
       
       
       {
//Chrome Setup to run tests in the chrome browser - comment in/out the two lines below.
      System.setProperty("webdriver.chrome.driver","C:\\browserdrivers\\chromedriver.exe");
      ChromeDriver driver = new ChromeDriver();
      
      
//Firefox Setup to run tests in the firefox browser - comment in/out the two lines below.
//    System.setProperty("webdriver.gecko.driver","C:\\browserdrivers\\geckodriver.exe");
//    FirefoxDriver driver = new FirefoxDriver();
           
           
//To open the browser
      driver.get("https://www.facebook.com/");
      
      
//To maximize the browser window
      driver.manage().window().maximize();
      
      
//To input the values in the the different fields/Send values into fields.
      driver.findElement(By.xpath("//*[@id=\"email\"]")).sendKeys("Mobile Number/Email-ID");
      
      driver.findElement(By.xpath("//*[@id=\"pass\"]")).sendKeys("Password");
/*
To perform mouse based operation-

//Click on the button/radio button/link/checkbox.
*/
           driver.findElement(By.xpath("//*[@id=\"u_0_b\"]")).click();
      
//Alert Interface Methods -
           
//1) Void dismiss()
//This method is called when the ‘Cancel’ button is clicked in the alert box.
      driver.switchTo().alert().dismiss();
      
//2) Void accept()
//This method is called when you click on the ‘OK’ button of the alert.
      driver.switchTo().alert().accept();
      
//3) String getText()
//This method is called to capture the alert message.
      driver.switchTo().alert().getText();
      
      
//4) Void sendKeys(String stringToSend)
//This is called when you want to send some data to alert box.
      driver.switchTo().alert().sendKeys("Text");
      }
{
}
    }
}



