package com.main.utils;

import java.util.HashMap;
import java.util.Map;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.chrome.ChromeOptions;
import org.openqa.selenium.edge.EdgeDriver;
import org.openqa.selenium.edge.EdgeOptions;


public class DriverSetup {
private static WebDriver driver;

    public static WebDriver getDriver(String br) {
    	driver=null;
        if (driver==null && br.equals("chrome")) {

//          🔕 Block Chrome notifications
             Map<String, Object> prefs = new HashMap<>();
             prefs.put("profile.default_content_setting_values.notifications", 2);

             ChromeOptions options = new ChromeOptions();
             options.setExperimentalOption("prefs", prefs);
             options.addArguments("--disable-notifications"); // extra layer
             driver = new ChromeDriver(options);

            driver.manage().window().maximize();
        }
        else if(driver==null &&  br.equals("edge"))
        {
//            🧪 Try disabling notifications via launch argument
                  EdgeOptions options = new EdgeOptions();
                  options.addArguments("--disable-notifications");

                 driver = new EdgeDriver(options);
             driver.manage().window().maximize();
        }
        else
        {
        	System.out.println("this is else");
//          🔕 Block Chrome notifications
            Map<String, Object> prefs = new HashMap<>();
            prefs.put("profile.default_content_setting_values.notifications", 2);

            ChromeOptions options = new ChromeOptions();
            options.setExperimentalOption("prefs", prefs);
            options.addArguments("--disable-notifications"); // extra layer
            driver = new ChromeDriver(options);
//        	driver = new ChromeDriver();
            driver.manage().window().maximize();
        }
        return driver;
    }

    public static void quitDriver() {
        if (driver != null) {
            driver.quit();
        }
    }
}