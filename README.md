# clarion11
assignment
package Tests;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;

public class clarion {

	public static void main(String[] args) {
		System.setProperty("webdriver.chrome.driver", "C:\\Sel\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
	      	driver.get("http://182.74.238.209/clarion_promise_qa/home.php");
			driver.manage().window().maximize();
			driver.findElement(By.xpath("//input[@name='txtUsername']")).sendKeys("sanjeetk@clariontechnologies.co.in");
			driver.findElement(By.xpath("//input[@name='txtPassword']")).sendKeys("clarion");
			driver.findElement(By.xpath("//input[@name='submit1']")).click();
			driver.findElement(By.xpath("//a[contains(text(),'Log Promise')]")).click();
				
			Select Promise_From = new Select(driver.findElement(By.xpath("//select[@name='cboEmp']")));
			Promise_From.selectByVisibleText("Sonali test");
			driver.findElement(By.xpath("//textarea[@id='txtPromise']")).sendKeys("Enter Promise");
			driver.findElement(By.xpath("//input[@id='btnSubmit']")).click();
			Select Promisor = new Select(driver.findElement(By.xpath("//select[@id='cboEmp']")));
			Promisor.selectByVisibleText("Sonali test");
			driver.findElement(By.xpath("//input[@name='btnSearch']")).click();
			driver.findElement(By.xpath("//b[contains(text(),'LOGOUT')]")).click();
			

		// TODO Auto-generated method stub

	}

}

