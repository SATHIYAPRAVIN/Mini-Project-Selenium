package com.main.TestBase;

import java.util.Map;

import org.testng.annotations.Test;
import com.main.pages.HomePage;
import com.main.pages.LoginPage;
import com.main.utils.ExcelUtils;

public class TC003_AuthenticationAndScreenShot extends BaseClass{
  @Test
	public void AuthenticationAndScreenShot() {
		Map<String, String> inputs = ExcelUtils.getInputsForKeyword("Authentication");
	    String email = inputs.get("emailValue");
	    String password = inputs.get("passwordValue");
	    System.out.println(email +"  and  "+password);
	    
	    HomePage home=new HomePage(driver);
	    home.clickLogin();
		System.out.println("^^^^^^^^^^start Authentication method in Test^^^^^^^^^^^^");
		LoginPage login=new LoginPage(driver); 
		login.googleAuthentication(email,password);
		System.out.println("^^^^^^^^^^Authentication method done in Test^^^^^^^^^^^^^");

		System.out.println("##############Start screenshot method in Test############");
		login.captureTestScreenshot();
		System.out.println("##############Screenshot method done in Test##############");
	}
	
}
