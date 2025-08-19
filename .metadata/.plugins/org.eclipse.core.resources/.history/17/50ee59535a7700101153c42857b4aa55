package com.main.pages;

import java.io.File;
import java.io.IOException;

import org.apache.commons.io.FileUtils;
import org.openqa.selenium.By;
import org.openqa.selenium.OutputType;
import org.openqa.selenium.TakesScreenshot;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.support.ui.ExpectedConditions;

public class LoginPage extends HomePage{
	private By Facebook=By.xpath("//*[@id=\"myModal3-modal-content\"]/div[1]/div/div[3]/div[4]/div[1]/span[2]");
	private By Email=By.xpath("//input[@id='email']");
	private By PasswordBy=By.xpath("//input[@id='pass']");
	private By Submitbtn=By.xpath("//input[@type='submit']");
	private By errorBox=By.xpath("//*[@id=\"error_box\"]");
	
	public LoginPage(WebDriver driver) {
		super(driver);
		System.out.println("login->>"+driver.getCurrentUrl());
		// TODO Auto-generated constructor stub
	}

	public void googleAuthentication(String EMail,String Password) {
    	// 1) Go to the homePage
//     	2)click loogin&More Button
		System.out.println("navigatedToHomepage for authentication->>"+driver.getCurrentUrl());
//     	3)click facebook Button
    	 keys.click(Facebook);
     	 keys.pause(2);
     	driver=keys.switchwindow(driver);//switch window
//      4)send Input for Email
     	 keys.enterText(Email,EMail);
//      5)send Input for password
     	 keys.enterText(PasswordBy,Password);
//      6)click the submitButton
     	 keys.click(Submitbtn);
//     7)Capture ErrorMessage
     	String ErrorMessage= keys.getText(errorBox);
//     8)print the error Message
     	System.out.println("ErrorMessage->>>"+ErrorMessage);
     }
	
	public  void captureTestScreenshot(){
    	wait.until(ExpectedConditions.visibilityOfElementLocated(By.xpath("//div[@class='pam login_error_box _9ay3 uiBoxRed']")));
    	TakesScreenshot screenshot=(TakesScreenshot) driver;
    	File src=screenshot.getScreenshotAs(OutputType.FILE);
     	File dest=new File("./Screenshots/error.png");
     	try {
     		FileUtils.copyFile(src, dest);
     		System.out.println("Screenshot captured");
     	}catch(IOException e) {
     		System.out.println(e.getMessage());
     	}
 	}
}
