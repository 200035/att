Week 1:  
Download and Install JAVA, Associate SWD Jars and Browser drivers.

Week 2:
Launch Mercury Tour website
a)  Click Register link to get registration page		b) Fill fields
c)  Click submit						d) Close site

Week 3:
Write a code to search a specific month in the Face book registration page (Birthday).

Week 4:  
Write a program which pops out an alert message in frame in personal banking login page.

Week 5:  
Write a test case to search result section on CMRIT Website.

Week 6:  
Write a test case to perform automation on Ajio shopping website.

Week 7:
Write a program in web driver to open Google and search CMRIT.


Week 8:  
Write test case to open Google and download a image from Google images of cmrit website.

Week 9:   
Write test case to get number of list items in a list.

Week 10:
  Write test case for validation in Gmail registration page.

Week11:
Write test case for myntra sign in page.

Week12:
Write test case to convert PDF from word.






Week 2(Mercury Home Tour)
package week02;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;
public class Mercury {
	public static void main(String[] args) throws InterruptedException {
System.setProperty("webdriver.chrome.driver","F:\\Lab\\chromedriver-win64\\chromedriver-win64\\chromedriver.exe");
WebDriver driver=new ChromeDriver();
driver.manage().window().maximize();
driver.get("https://www.mercurytravels.co.in/");
Thread.sleep(2000);
Actions builder = new Actions(driver);
WebElement customerLogin =	driver.findElement(By.xpath("(//a[normalize-space()='Customer Login'])[2]"));
builder.moveToElement(customerLogin).perform();
Thread.sleep(2000);
WebElement register = driver.findElement(By.xpath("(//a[normalize-space()='Register'])[2]"));
register.click();
Thread.sleep(2000);
WebElement firstName = driver.findElement(By.id("acc_first_name"));
firstName.sendKeys("DeekshithChary");
Thread.sleep(2000);
WebElement lastName = driver.findElement(By.id("acc_last_name"));
lastName.sendKeys("P");
Thread.sleep(2000);
WebElement emailId = driver.findElement(By.id("acc_user_email"));
emailId.sendKeys("Deekshithchary0607@gmail.com");
Thread.sleep(2000);
WebElement setPassword = driver.findElement(By.id("acc_user_password"));
setPassword.sendKeys("12345");
Thread.sleep(2000);
WebElement confirmPassword = driver.findElement(By.id("acc_user_passconf"));
confirmPassword.sendKeys("12345");
Thread.sleep(2000);
WebElement mobileNumber = driver.findElement(By.id("acc_mobile_no"));
mobileNumber.sendKeys("8124563783");
Thread.sleep(2000);
WebElement registerBtn = driver.findElement(By.xpath("(//button[normalize-space()='Register'])"));
registerBtn.click();
Thread.sleep(1000);
}
}

Week 03(Facebook Validation)
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;
import org.openqa.selenium.support.ui.Select;
public class FacebookReg {
	public static void main(String[] args) throws InterruptedException  {
System.setProperty("webdriver.chrome.driver", "F:\\Lab\\Updated\\chromedriver-win64\\chromedriver.exe");
WebDriver driver=new ChromeDriver();
driver.get("https://www.facebook.com/");
Thread.sleep(200);
driver.findElement(By.partialLinkText("Create new account")).click();
Thread.sleep(500);
driver.findElement(By.name("firstname")).sendKeys("ashu");
Thread.sleep(500);
WebElement surName = driver.findElement(By.name("lastname"));
surName.sendKeys("kamatam");
Thread.sleep(500);
WebElement mobileNoOrEmailId= driver.findElement(By.name("reg_email__"));
mobileNoOrEmailId.sendKeys("1234567890");
Thread.sleep(500);
WebElement password = driver.findElement(By.name("reg_passwd__"));
password.sendKeys("123ashu");
Select dateDropdown = new Select(driver.findElement(By.name("birthday_day")));
dateDropdown.selectByValue("24");
Thread.sleep(500);
Select monthDropdown = new Select(driver.findElement(By.name("birthday_month")));
monthDropdown.selectByValue("12");
Thread.sleep(500);
Select yearDropdown = new Select(driver.findElement(By.name("birthday_year")));
yearDropdown.selectByValue("1996");
Thread.sleep(500);
WebElement femaleRadioBtn = driver.findElement(By.xpath("(//label[normalize-space()='Female'])[1]"));
femaleRadioBtn.click();
Thread.sleep(500);
WebElement signUpBtn = driver.findElement(By.name("websubmit"));
signUpBtn.click();
	}
}

Method-02
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;
public class FacebookReg01 {
	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", "F:\\Lab\\Updated\\chromedriver-win64\\chromedriver.exe");
		WebDriver driver=new ChromeDriver();
		driver.get("https://www.facebook.com/");
		Thread.sleep(200);
		WebElement createAccount=driver.findElement(By.xpath("(//a[normalize-space()='Create new account'])[1]"));
		createAccount.click();
		Thread.sleep(500);
		driver.findElement(By.name("firstname")).sendKeys("ashu");
		Thread.sleep(500);
		WebElement surName = driver.findElement(By.name("lastname"));
		surName.sendKeys("kamatam");
		Thread.sleep(500);
		WebElement mobileNoOrEmailId= driver.findElement(By.name("reg_email__"));
		mobileNoOrEmailId.sendKeys("1234567890");
		Thread.sleep(500);
		WebElement password = driver.findElement(By.name("reg_passwd__"));
		password.sendKeys("123ashu");
		Select dateDropdown = new Select(driver.findElement(By.name("birthday_day")));
		dateDropdown.selectByValue("24");
		Thread.sleep(500);
		Select monthDropdown = new Select(driver.findElement(By.name("birthday_month")));
		monthDropdown.selectByValue("12");
		Thread.sleep(500);
		Select yearDropdown = new Select(driver.findElement(By.name("birthday_year")));
		yearDropdown.selectByValue("1996");
		Thread.sleep(500);
		WebElement femaleRadioBtn = driver.findElement(By.xpath("(//label[normalize-space()='Female'])[1]"));
		femaleRadioBtn.click();
		Thread.sleep(500);
		WebElement signUpBtn = driver.findElement(By.name("websubmit"));
		signUpBtn.click();

	}

}




Week 04(Popup Bank Notification)
import java.util.HashMap;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.chrome.ChromeOptions;
//import org.openqa.selenium.chrome.ChromeOptions;
public class Week04 {
	public static void main(String[] args) {
		HashMap<String, Object> prefs=new HashMap<String, Object>();
		prefs.put("profile.default_content_setting_values.notifications",0);
		ChromeOptions options=new ChromeOptions();
		options.setExperimentalOption("prefs", prefs);
		System.setProperty("webdriver.chrome.driver","F:\\Lab\\chromedriver\\chromedriver.exe");
		WebDriver driver=new ChromeDriver(options);
		driver.manage().window().maximize();
		driver.get("https://www.axisbank.com/");
		WebElement pop=driver.findElement(By.xpath("/html/body/div[1]/div[1]/div/span"));
		pop.click();
	}
	}












Week 05(Cmrit Bees Results)
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
public class Week5 {
	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver","F:\\Lab\\chromedriver\\chromedriver.exe");
		WebDriver driver=new ChromeDriver();
		driver.manage().window().maximize();
		driver.get("https://cmritautonomous.org/beeserp/Login.aspx");
		WebElement userName=driver.findElement(By.name("txtUserName"));
		userName.sendKeys("20R01A05K6P");
		Thread.sleep(2000);
		WebElement nxtBtn=driver.findElement(By.name("btnNext"));
  		nxtBtn.click();
		WebElement password=driver.findElement(By.name("txtPassword"));
		password.sendKeys("20R01A05K6P");
		Thread.sleep(2000);
		WebElement submit=driver.findElement(By.name("btnSubmit"));        
		submit.click();
	}
}       











Week-6 (Perform automation on Ajio shopping website)
import java.util.Iterator;
import java.util.Set;
import org.openqa.selenium.By;                                                                                
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;
public class wk {
public static void main(String[] args) throws InterruptedException  {
System.setProperty("webdriver.chrome.driver", "F:\\Lab\\Updated\\chromedriver-win64\\chromedriver.exe");
WebDriver driver=new ChromeDriver();
driver.get("https://www.ajio.com/");
Thread.sleep(2000);
WebElement ajioLink = driver.findElement(By.xpath("//span[normalize-space()='Sign In / Join AJIO']"));
ajioLink.click();
Thread.sleep(2000);
WebElement facebookBtn = driver.findElement(By.xpath("//span[normalize-space()='Facebook']"));
facebookBtn.click();
Thread.sleep(2000);
Set<String> parentWindow = driver.getWindowHandles();
Iterator iterator = parentWindow.iterator();
while(iterator.hasNext())
{
String childWindow = (String) iterator.next();
if(!parentWindow.equals(childWindow))
{
driver.switchTo().window(childWindow);
}
}
WebElement emailOrMobileNo =driver.findElement(By.xpath("//input[@id='email']"));
emailOrMobileNo.sendKeys("bhumi27@gmail.com");
WebElement pwd = driver.findElement(By.xpath("//input[@id='pass']"));
pwd.sendKeys("@123");
WebElement loginBtn = driver.findElement(By.xpath("/html/body/div/div[2]/div[1]/form/div/div[4]/label[2]/input"));
loginBtn.click();
}
}

Week 07(Web Driver google Search Cmrit)
import org.openqa.selenium.By;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
public class Week7 {
	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", "F:\\Lab\\chromedriver\\chromedriver.exe");
	WebDriver driver=new ChromeDriver();
	driver.manage().window().maximize();
	driver.get("https://www.google.com/");
	Thread.sleep(2000);
	WebElement searchBar= driver.findElement(By.name("q"));
	searchBar.sendKeys("cmrit hyderabad");
	searchBar.sendKeys(Keys.ENTER);
	Thread.sleep(15000);   
	driver.quit();
		}
	}




Week-08(Cmrit Image Download)
import java.awt.AWTException;
import java.awt.Robot;
import java.awt.event.KeyEvent;
import org.openqa.selenium.By;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;
public class Image {
	public static void main(String[] args)  throws InterruptedException, AWTException {
		WebDriver driver=new ChromeDriver();
		driver.manage().window().maximize();
		driver.get("https://www.google.com");
		Thread.sleep(2000);
		WebElement searchBar=driver.findElement(By.name("q"));
		searchBar.sendKeys("cmrit hyderabad");
		searchBar.sendKeys(Keys.ENTER);
		Thread.sleep(15000);
		WebElement img=driver.findElement(By.xpath("//a[normalize-space()='Images']"));
		img.click();
		WebElement img1=driver.findElement(By.xpath("//img[@alt='CMR Institute of Technology, Hyderabad Courses & Fees 2023']"));
		Actions action = new Actions(driver);
		action.contextClick(img1).build().perform();
		Robot robot=new Robot();
		robot.keyPress(KeyEvent.VK_DOWN);
		Thread.sleep(2000);
		robot.keyPress(KeyEvent.VK_DOWN);
		Thread.sleep(2000);
		robot.keyPress(KeyEvent.VK_DOWN);
		Thread.sleep(2000);
		robot.keyPress(KeyEvent.VK_DOWN);
		Thread.sleep(2000);
		robot.keyPress(KeyEvent.VK_DOWN);
		Thread.sleep(2000);
		robot.keyPress(KeyEvent.VK_DOWN);
		Thread.sleep(2000);
		robot.keyPress(KeyEvent.VK_DOWN);
		Thread.sleep(2000);
		robot.keyPress(KeyEvent.VK_ENTER);
		Thread.sleep(3000);
		robot.keyPress(KeyEvent.VK_ENTER);
		System.out.println("downloaded");
		// driver.close();
		}
		}

Week 09(List items)
package week09;
import java.util.List;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
public class ListItems {
public static void main(String[] args) {
System.setProperty("webdriver.chrome.driver","F:\\Lab\\chromedriver-win64\\chromedriver-win64\\chromedriver.exe");
WebDriver driver=new ChromeDriver();
driver.manage().window().maximize();
driver.get("https://www.justdial.com/Hyderabad/Bakeries/nct-10033880");
List<WebElement> m = driver.findElements(By.xpath("//h2[@class='jsx-3349e7cd87e12d75 resultbox_title font22 fw500 color111 complist_title']"));
for(int i = 0; i< m.size(); i++) {
String s = m.get(i).getText();
System.out.println("Text is: " + s);
	      }

	}
	}

Week 10 (Gmail Validation)
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;
public class exp10 {
	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", "F:\\Lab\\Updated\\chromedriver-win64\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.get("http://gmail.com/");
		Thread.sleep(2000);
		WebElement createAccount = driver.findElement(By.xpath("(//span[normalize-space()='Create account'])[1]"));
		createAccount.click();
		Thread.sleep(2000);
		WebElement mySelft = driver.findElement(By.xpath("(//span[normalize-space()='For my personal use'])[1]"));
		mySelft.click();
		Thread.sleep(2000);
		WebElement firstName = driver.findElement(By.name("firstName"));
		firstName.sendKeys("Kumar01");
		Thread.sleep(2000);
		WebElement lastName = driver.findElement(By.name("lastName"));
		lastName.sendKeys("Ravi");
		Thread.sleep(2000);
		WebElement bn1 = driver.findElement(By.xpath("(//span[normalize-space()='Next'])"));
		bn1.click();
		Thread.sleep(3000);
		  Select month = new Select(driver.findElement(By.xpath("(//select[@id='month'])[1]")));
		  month.selectByValue("8");
		  Thread.sleep(2000);
		  WebElement day = driver.findElement(By.xpath("(//input[@id='day'])[1]"));
		  day.sendKeys("24");
		  Thread.sleep(2000);
		  WebElement year = driver.findElement(By.xpath("(//input[@id='year'])[1]"));
		  year.sendKeys("1996");
		  Select gender = new
		  Select(driver.findElement(By.xpath("(//select[@id='gender'])[1]")));
		  gender.selectByValue("1");
		  Thread.sleep(2000);
		  WebElement bn2 = driver.findElement(By.xpath("(//span[normalize-space()='Next'])"));
		  bn2.click();
		  Thread.sleep(2000);
		  WebElement uid = driver.findElement(By.name("Username"));
		  uid.sendKeys("Kmrthakla");
		  WebElement bn3 = driver.findElement(By.xpath("(//span[normalize-space()='Next'])"));
		  bn3.click();
		  Thread.sleep(2000);
		  WebElement pswd = driver.findElement(By.name("Passwd"));
		  pswd.sendKeys("Cmrit123#");
		  WebElement cpswd = driver.findElement(By.name("PasswdAgain"));
		  cpswd.sendKeys("Cmrit123#");
		  WebElement bn4 = driver.findElement(By.xpath("(//span[normalize-space()='Next'])"));
		  bn4.click();
	}
	}








Week 11 (Myntra)
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;
public class Myntra {
public static void main(String[] args) throws InterruptedException  {
	System.setProperty("webdriver.chrome.driver", "F:\\Lab\\Updated\\chromedriver-win64\\chromedriver.exe");
	WebDriver driver=new ChromeDriver();
	Actions builder = new Actions(driver);
	driver.get("https://www.google.co.in/");
	WebElement searchBar = driver.findElement(By.name("q"));
	searchBar.sendKeys("Myntra");
	Thread.sleep(500);
	searchBar.submit();	WebElement myntraLink = driver.findElement(By.xpath("(//h3[contains(text(),'Myntra: Online Shopping for Women, Men, Kids Fashi')])[1]"));
	myntraLink.click();
	WebElement profileHyperLink = driver.findElement(By.xpath("(//span[normalize-space()='Profile'])[1]"));
	profileHyperLink.click();
	WebElement loginBtn = driver.findElement(By.xpath("(//a[normalize-space()='login / Signup'])[1]"));
	loginBtn.click();
	WebElement mobileNo = driver.findElement(By.xpath("(//input[@type='tel'])[1]"));
	mobileNo.sendKeys("9948621019");
	WebElement continueBtn = driver.findElement(By.xpath("(//div[@class='submitBottomOption'])[1]"));
	continueBtn.click();
	Thread.sleep(500);
//	WebElement otp01 = driver.findElement(By.xpath("(//input[@name='otp0'])[1]"));
//	otp01.sendKeys("1");
//	WebElement otp02 = driver.findElement(By.xpath("(//input[@name='otp1'])[1]"));
//	otp02.sendKeys("2");
//	WebElement otp03 = driver.findElement(By.xpath("(//input[@name='otp2'])[1]"));
//	otp03.sendKeys("3");
//	WebElement otp04 = driver.findElement(By.xpath("(//input[@name='otp3'])[1]"));
//	otp04.sendKeys("4");
//	driver.close();
	}
}
Week 12(Pdf To Word Convertor)
import java.awt.AWTException;
import java.awt.Robot;
import java.awt.Toolkit;
import java.awt.datatransfer.Clipboard;
import java.awt.datatransfer.StringSelection;
import java.awt.event.KeyEvent;
import org.openqa.selenium.By;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
public class PdftoWord {
	public static void main(String[] args) throws InterruptedException, AWTException {
System.setProperty("webdriver.chrome.driver", "F:\\Lab\\Updated\\chromedriver-win64\\chromedriver.exe");
WebDriver driver= new ChromeDriver();
driver.get("https://www.google.com/");
Thread.sleep(2000);
WebElement searchBar = driver.findElement(By.name("q"));
searchBar.sendKeys("Convert pdf to word online");
searchBar.sendKeys(Keys.ENTER);
WebElement pdfToWord = driver.findElement(By.xpath("(//h3[@class='LC20lb MBeuO DKV0Md'])[2]"));
pdfToWord.click();
Thread.sleep(500);
WebElement chooseFileBtn = driver.findElement(By.xpath("(//span[normalize-space()='Choose Files'])[1]"));
chooseFileBtn.click();
Thread.sleep(500);	
Clipboard clipboard = Toolkit.getDefaultToolkit().getSystemClipboard();
StringSelection str = new StringSelection("Downloads\\01.pdf");
clipboard.setContents(str,null);
Thread.sleep(500);
Robot robot = new Robot();
robot.keyPress(KeyEvent.VK_CONTROL);
robot.keyPress(KeyEvent.VK_V);
robot.keyPress(KeyEvent.VK_ENTER);
Thread.sleep(500);
WebElement convertToWord = driver.findElement(By.xpath("(//div[@class='sc-6ytb27-2 guQZea'])[1]"));
convertToWord.click();
WebElement choosePlan =
driver.findElement(By.xpath("(//span[@class='r5zwp6-3 iiSRjo'])[3]"));
choosePlan.click();
Thread.sleep(10000);
WebElement download = driver.findElement(By.xpath("(//span[@class='r5zwp6-3 iiSRjo'])[4]"));
download.click();
}	
}

