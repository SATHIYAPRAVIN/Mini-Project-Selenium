package com.main.TestBase;

import java.util.Map;
import org.testng.annotations.Test;
import com.main.pages.HomePage;
import com.main.pages.UpcomingBikes;
import com.main.utils.ExcelUtils;

public class TC001_UpcomingBikes extends BaseClass{
 
	
  @Test
	  public void Filter() throws InterruptedException {
	  Map<String, String> inputs = ExcelUtils.getInputsForKeyword("FilterMethod");
		   String brand = inputs.get("brandName");
		   String maxPrice = inputs.get("maxPrice");
		   System.out.println(brand +"  and  "+maxPrice);
		   HomePage home=new HomePage(driver);
		   home.clickNewBikes();
		   UpcomingBikes upcoming=new UpcomingBikes(driver);

			System.out.println("********start Filter method in Test**********");
			upcoming.FilterMethod(brand,maxPrice);
			System.out.println("********Filter method done in Test***********");
  }
}
