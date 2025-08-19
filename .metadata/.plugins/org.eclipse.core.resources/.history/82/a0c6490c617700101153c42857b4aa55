package com.main.pages;

import java.util.List;
import org.openqa.selenium.By;
import org.openqa.selenium.JavascriptExecutor;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.support.ui.ExpectedConditions;

public class UpcomingBikes extends HomePage{
    private By UpcomingBikes=By.xpath("//li[text()='Upcoming']");
    private By AdvancedSearch=By.xpath("//a[text()='Advanced Search ']");
    private By Viewall=By.xpath("//a[text()=\"View All \"]");
    private By Searchbtn=By.id("searchMake_submit");
    private By MaxPrice=By.id("maxPrice");
    private By LoadMore=By.xpath("//div[@class=\"text-center mb-15 mt-15 load_more_btn\"]/span");
	private By Brand=By.xpath("//ul[@class='zw-sr-secLev mt-10 popupheight']/li");
	private By BikeName=By.tagName("strong");
    private By BikePrice=By.xpath("//div[@class='clr-bl p-5']");

	public UpcomingBikes(WebDriver driver) {
		super(driver);
		// TODO Auto-generated constructor stub
	}
	
	public void FilterMethod(String BrandNamePar,String MaxPricePar) throws InterruptedException{
//	    1)click the NewBikes link in header
		 driver=keys.switchwindow(driver);//switch window
	      System.out.println("switch"+driver.getCurrentUrl());
//	    2)click the upcomingBikes link
	   	  keys.click(UpcomingBikes);
//	 	  3)move to element advanceSearch and click it
	      keys.hover(AdvancedSearch);
	      keys.pause(2);
	      keys.click(AdvancedSearch);
	      driver=keys.switchwindow(driver);//switch window
//	    4)click the element viewAll 
	      keys.hover(Viewall);
	      keys.click(Viewall);
//	 	  5)select the Honda option
	   	  List<WebElement> brand=wait.until(ExpectedConditions.visibilityOfAllElementsLocatedBy(Brand));
	   	  for(WebElement b:brand) {
	   		 WebElement brandele=b.findElement(By.xpath(".//label"));
	   		 String BrandName=brandele.getText().trim();
	   		    if(BrandName.equalsIgnoreCase(BrandNamePar)) {
	   		    	brandele.click();
	   		    	break;
	   		    }
	   	  }
	//   6)click the search button after selecting the Honda button
	   	 keys.click(Searchbtn);
	     System.out.println("Selected Brand--> "+driver.getCurrentUrl());
	//   7)click on the maxPrice dropDown and select the 4lakhs option
	     keys.scrollIntoView(MaxPrice);
	     keys.slowDown(1);
	     keys.selectDropdown(MaxPrice, MaxPricePar);
	     System.out.println("Selected MaxPrice--> "+driver.getCurrentUrl());
	//   8)click loadmore button and display the bike details
	         keys.hover(LoadMore );
//	         keys.click("xpath","//div[@class=\"text-center mb-15 mt-15 load_more_btn\"]/span" );
	         WebElement Ele=keys.getWebElement(LoadMore);
	         ((JavascriptExecutor) driver).executeScript("arguments[0].click();",Ele);
	         keys.slowDown(1);
	         ((JavascriptExecutor) driver).executeScript("window.scrollTo(0, 0);");//scroll to top
	         System.out.println("Fetching bike details...................");
	         keys.pause(1);
	         List<WebElement> name=wait.until(ExpectedConditions.visibilityOfAllElementsLocatedBy(BikeName));
	         List<WebElement> Price=wait.until(ExpectedConditions.visibilityOfAllElementsLocatedBy(BikePrice));
	         keys.slowDown(1); 
		      for(int i=0;i<name.size();i++) {
		    	  System.out.println(i+"->> "+name.get(i).getText()+"->>"+Price.get(i).getText());
		      }
		      keys.slowDown(1);     
	     }
	  

}
