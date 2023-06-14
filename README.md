import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.chrome.ChromeOptions;
import org.openqa.selenium.support.ui.ExpectedConditions;
import org.openqa.selenium.support.ui.WebDriverWait;
import org.openqa.selenium.JavascriptExecutor;
import org.openqa.selenium.Keys;
import org.apache.poi.ss.usermodel.*;
import org.apache.poi.xssf.usermodel.XSSFWorkbook;
import java.io.FileInputStream;
import java.io.IOException;
public class SauceDemoAutomation {
    public static void main(String[] args) {
System.setProperty("webdriver.chrome.driver", "path_to_chromedriver");
WebDriver driver = new ChromeDriver(options);
driver.get("https://www.saucedemo.com/");
//WebElement usernameInput = driver.findElement(By.id("user-name"));
//WebElement passwordInput = driver.findElement(By.id("password"));
//WebElement loginButton = driver.findElement(By.cssSelector("input[value='LOGIN']"));
//ChromeOptions options = new ChromeOptions();
//options.addArguments("--start-maximized");
//WebDriverWait wait = new WebDriverWait(driver, 10);
//JavascriptExecutor jsExecutor = (JavascriptExecutor) driver;
//String filePath = "path_to_excel_file";
//String sheetName = "Sheet1";
//String usernameColumn = "Username";
//String passwordColumn = "Password";

//Workbook workbook = new XSSFWorkbook(new FileInputStream(filePath));
//Sheet sheet = workbook.getSheet(sheetName);

//Row headerRow = sheet.getRow(0);
//int usernameColumnIndex = headerRow.getCell(usernameColumn).getColumnIndex();
//int passwordColumnIndex = headerRow.getCell(passwordColumn).getColumnIndex();

//Row credentialsRow = sheet.getRow(1);
//String username = credentialsRow.getCell(usernameColumnIndex).getStringCellValue();
//String password = credentialsRow.getCell(passwordColumnIndex).getStringCellValue();

workbook.close();

//WebElement usernameField = wait.until(ExpectedConditions.visibilityOfElementLocated(By.id("user-name")));
//usernameField.sendKeys(username);

//WebElement passwordField = driver.findElement(By.id("password"));
//passwordField.sendKeys(password);

//WebElement loginButton = driver.findElement(By.id("login-button"));
//loginButton.click();

//WebElement inputField = driver.findElement(By.id("input-field"));
//inputField.sendKeys("Invalid value");
//WebElement errorMessage = driver.findElement(By.id("error-message"));

// Assert the error message is displayed
assert(errorMessage.isDisplayed());

// Validate the error message text
assert(errorMessage.getText().equals("Invalid value"));

//WebElement sortDropdown = wait.until(ExpectedConditions.visibilityOfElementLocated(By.className("product_sort_container")));
//sortDropdown.click();

//WebElement sortOption = driver.findElement(By.xpath("//option[@value='lohi']"));
//sortOption.click();
//List<WebElement> addToCartButtons = driver.findElements(By.xpath("//button[contains(text(),'Add to cart')]"));
//for (WebElement button : addToCartButtons) {
    button.click();
}
//WebElement cartLink = driver.findElement(By.className("shopping_cart_link"));
//cartLink.click();

//List<WebElement> cartItems = driver.findElements(By.className("cart_item"));

//for (WebElement item : cartItems) {
    //WebElement priceElement = item.findElement(By.className("inventory
  //java.util.List<WebElement> cartItems = driver.findElements(By.cssSelector(".cart_item"));
        //for (WebElement item : cartItems) {
            //String priceText = item.findElement(By.cssSelector(".inventory_item_price")).getText();
            //double price = Double.parseDouble(priceText.substring(1)); // Remove the dollar sign and convert to double
            //if (price < 15.0) {
                //WebElement removeButton = item.findElement(By.cssSelector("button.cart_button"));
                //removeButton.click();
            }
        }
// Go to the Checkout page
        WebElement checkoutButton = driver.findElement(By.cssSelector(".checkout_button"));
        checkoutButton.click();
   // Enter details on the information page
        WebElement firstNameInput = driver.findElement(By.id("first-name"));
        WebElement lastNameInput = driver.findElement(By.id("last-name"));
        WebElement postalCodeInput = driver.findElement(By.id("postal-code"));
        WebElement continueButton = driver.findElement(By.cssSelector("input[value='CONTINUE']"));

        firstNameInput.sendKeys("Your First Name");
        lastNameInput.sendKeys("Your Last Name");
        postalCodeInput.sendKeys("585629");
        continueButton.click();

        // Finish the checkout
        WebElement finishButton = driver.findElement(By.cssSelector("a.btn_action.cart_button"));
        finishButton.click();

        // Return to the home page
        WebElement backToHomeButton = driver.findElement(By.cssSelector("button.cart_button"));
        backToHomeButton.click();

        // Perform logoutbackToHomeButton.click();

        // Perform logout
        WebElement menuButton = driver.findElement(By.cssSelector(".bm-burger-button"));
        menuButton.click();
        WebElement logoutLink = driver.findElement(By.id("logout_sidebar_link"));
        logoutLink.click();

        // Wait for a while before closing the browser

       
        
                            
