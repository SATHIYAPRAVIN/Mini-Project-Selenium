package com.main.utils;
import java.time.Duration;
import java.util.Set;

import org.openqa.selenium.*;
import org.openqa.selenium.interactions.Actions;
import org.openqa.selenium.support.ui.*;

public class KeywordActions {

    WebDriver driver;
    WebDriverWait wait;
    static String parenthandle;
    
    
    
    public KeywordActions(WebDriver driver) {
        this.driver = driver;
        this.wait = new WebDriverWait(driver, Duration.ofSeconds(50));
    }
    
    public WebElement getWebElement(By by) {
       return wait.until(ExpectedConditions.visibilityOfElementLocated(by));
    }
    
    public void click(By by) {

        wait.until(ExpectedConditions.elementToBeClickable(by)).click();
    }

    public void enterText(By by, String text) {

        wait.until(ExpectedConditions.visibilityOfElementLocated(by)).sendKeys(text);
    }
    public String getText(By by) {

        return wait.until(ExpectedConditions.visibilityOfElementLocated(by)).getText();
    }

   public void hover(By by) {
        WebElement element = wait.until(ExpectedConditions.visibilityOfElementLocated(by));
         new Actions(driver).moveToElement(element).perform();
     }


     public void scrollIntoView(By by) {
        WebElement element = wait.until(ExpectedConditions.visibilityOfElementLocated(by));
        ((JavascriptExecutor) driver).executeScript("arguments[0].scrollIntoView({behavior: 'smooth', block: 'start'});", element);
//        ((JavascriptExecutor) driver).executeScript("arguments[0].scrollIntoView(true);", element);
      }

    public void selectDropdown(By by, String value) {
        WebElement element = wait.until(ExpectedConditions.visibilityOfElementLocated(by));
        Select select = new Select(element);
        select.selectByValue(value);
    }
   
    public WebDriver switchwindow(WebDriver driver) {
      	   parenthandle=driver.getWindowHandle();
      	   Set<String> handles=driver.getWindowHandles();
      	   for(String i:handles) {
      		   if(!i.equalsIgnoreCase(parenthandle)) {
      			   driver.switchTo().window(i);
      		   }
      	   }
      	   System.out.println(driver.getCurrentUrl());         
         return driver;
    }
    
    public void slowDown(int secs) {
   	 (new Actions(driver)).pause(Duration.ofSeconds(secs)).perform();
	}
    
    public void pause(int secs) {
        try {
            Thread.sleep(secs * 1000L);
        } catch (InterruptedException ignored) { }
    }
}
