# Slic4r
package com.testscenaios;

import org.testng.annotations.Test;

import com.objectrepository.Locators;
import com.utilities.CommenFunctions;

public class TS_003_Verify_the_Forgot_PassWord extends CommenFunctions{
	
	Locators bb =new Locators();
	 CommenFunctions cfn =new   CommenFunctions();
	@Test(groups = { "sanity"})
	public void TC_015_Verify_the_Forgot_password_functionlity_with_blank_data() throws Exception {
		 cfn.ChromeBrowserLunch();
			driver.get("https://slic4rfe-ng-ngx.fabheads.in/register");
			Thread.sleep(3000);
			cfn.clickByAnyLocator(bb.Forgot_password_Link);
			cfn.clickByAnyLocator(bb.Forgot_password_Arrow_Symbol);
			driver.quit();
		
	}
	@Test(groups = { "sanity" })
	public void TC_016_Verify_the_Forgot_password_functionlity_with_invalid_data() throws Exception {
		 cfn.ChromeBrowserLunch();
			driver.get("https://slic4rfe-ng-ngx.fabheads.in/register");
			Thread.sleep(3000);
			cfn.clickByAnyLocator(bb.Forgot_password_Link);
			cfn.sendkeyByAnyLocator(bb.Forgot_password_Mail_TestBox, "jtyink34@fabheads.com");
			cfn.clickByAnyLocator(bb.Forgot_password_Arrow_Symbol);
			driver.quit();
		
	}
	@Test(groups = { "sanity"})
	public void TC_017_Verify_the_Forgot_password_functionlity_with_valid_data() throws Exception {
		 cfn.ChromeBrowserLunch();
			driver.get("https://slic4rfe-ng-ngx.fabheads.in/register");
			Thread.sleep(3000);
			cfn.clickByAnyLocator(bb.Forgot_password_Link);
			// provide valid mail id
			cfn.sendkeyByAnyLocator(bb.Forgot_password_Mail_TestBox, "jyothi@fabheads.com");
			cfn.clickByAnyLocator(bb.Forgot_password_Arrow_Symbol);
			driver.quit();
		
	}
}
