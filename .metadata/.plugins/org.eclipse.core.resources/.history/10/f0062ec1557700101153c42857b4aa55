package com.main.pages;

import java.time.Duration;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.interactions.Actions;
import org.openqa.selenium.support.PageFactory;
import org.openqa.selenium.support.ui.WebDriverWait;

import com.main.utils.KeywordActions;
public class HomePage{
    public WebDriver driver;
    public KeywordActions keys;
    public WebDriverWait wait;
    
    private By NewBikes=By.xpath("//a[text()='NEW BIKES']");
    private By dropdownBy=By.cssSelector("span.c-p.icon-down-arrow");
    private By login=By.xpath( "//*[@id='forum_login_title_lg']");
    
    public HomePage(WebDriver driver) {
    	this.driver=driver;
    	this.keys=new KeywordActions(driver);
    	PageFactory.initElements(driver, this);
    	this.wait = new WebDriverWait(driver, Duration.ofSeconds(50));
    }
    
    public void clickNewBikes() {
        keys.click(NewBikes);
    }
    
    public void clickMore() {
    	
    	WebElement dropdown=keys.getWebElement(dropdownBy);
    	
//       Hover over that arrow so the “Used Cars” link appears
        (new Actions(driver))
          .moveToElement(dropdown)
          .pause(Duration.ofMillis(100))
          .perform();
    }
    
    public void clickLogin() {
    	keys.click(login);
    }
    
}
