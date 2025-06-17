import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class SeleniumExample {

    public static void main(String[] args) {
        // Set the path to the ChromeDriver executable
        System.setProperty("webdriver.chrome.driver", "/path/to/chromedriver");

        // Initialize the ChromeDriver
        WebDriver driver = new ChromeDriver();

        // Navigate to a website
        driver.get("https://www.example.com");

        // Find an element by its ID
        WebElement element = driver.findElement(By.id("someElementId"));

        // Perform an action on the element
        element.sendKeys("some text");

        // Find an element by its CSS selector
        WebElement button = driver.findElement(By.cssSelector("button.someButtonClass"));

        // Perform an action on the element
        button.click();

        // Get the title of the page
        String title = driver.getTitle();
        System.out.println("Page title: " + title);

        // Close the browser
        driver.quit();
    }
}
