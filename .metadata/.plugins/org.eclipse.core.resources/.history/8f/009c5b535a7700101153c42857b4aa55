package com.main.pages;

import java.util.List;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;

public class ChennaiBikes extends HomePage{
	private By UsedCars=By.xpath("//a[@title='Used Cars']");
	private By Chennai=By.xpath("//a[@data-city_id='280']");
	private By scrollContainerBy=By.className("gsc_thin_scroll");
	
	public ChennaiBikes(WebDriver driver) {
		super(driver);
		System.out.println("chennaibikes-> "+driver.getCurrentUrl());
		// TODO Auto-generated constructor stub
	}
	
	public void usedCars() {
//      1) Go to the homePage
//      2) Wait for and locate the arrow icon (handles multiple classes)
//       3) Hover over that arrow so the “Used Cars” link appears
		
		System.out.println("navigatedToHomepage for displayChennaiLocation"+driver.getCurrentUrl());
        
      // 4) Now wait for and click the “Used Cars” submenu item
         keys.click(UsedCars);
         keys.click(Chennai);
         
         keys.slowDown(1);
      // 5) Find the scroll container once
         WebElement scrollContainer =keys.getWebElement(scrollContainerBy);
         keys.slowDown(1);
         keys.scrollIntoView(scrollContainerBy);
      // 6) Grab each <li> inside it
         List<WebElement> models = scrollContainer.findElements(
             By.tagName("li")
         );
         keys.slowDown(1);
      // 7) Loop and print each model’s text
         int i=1;
         for (WebElement model : models) {
             System.out.println(i+"-->>Popular Models In Chennai: " + model.getText());
             i++;
         }
         keys.slowDown(1);
     }

}
