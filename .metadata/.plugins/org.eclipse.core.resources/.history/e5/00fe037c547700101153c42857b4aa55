package com.main.TestBase;

import java.time.Duration;

import org.openqa.selenium.WebDriver;
import org.testng.annotations.AfterClass;
import org.testng.annotations.BeforeClass;
import org.testng.annotations.Optional;
import org.testng.annotations.Parameters;

import com.main.utils.DriverSetup;

	public class BaseClass {
		WebDriver driver;
		
		@BeforeClass
		@Parameters({"browser"})
		public void initDriver(@Optional ("edge") String br) {
			driver=DriverSetup.getDriver(br);
			driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(20));
			driver.get("https://www.zigwheels.com");	
		}


		  @AfterClass
		  public void afterClass() {
			  driver.quit();
		  }
	  }

