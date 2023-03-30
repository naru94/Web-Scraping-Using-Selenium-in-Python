# Web Scraping Using Selenium in Python
### Project Description
This project involves web scraping data from Wikipedia, the fastest growing free online encyclopedia using the Selenium library in Python. The project demonstrates how to use various Selenium commands to fetch HTML elements such as CSS class names, CSS IDs, HTML tag names, Link texts, Texts, Nested CSS selectors, and Attributes. It also covers how to use multiple Selenium events to automate processes on the website and how to clean the text data using regex library.

### Steps
#### 1. Import Libraries
* Import the following libraries: `Options`, `By`, `webdriver`, and `Service` from the `Selenium` package.
* Import `ChromeDriverManager` from the `webdriver_manager` package.
#### 2. Create Chrome WebDriver Instance
* Create an instance `wd` of Chrome WebDriver.
* Set the following options while creating the Chrome WebDriver instance:
  * Run the Selenium tests using a headless browser.
  * Disable the Sandbox mode.
  * Disable the Dev SHM mode.
#### 3. Automate Website Loading Event
* Go to the Wikipedia homepage using the `get()` method to navigate to a URL.
* Use an assertion method to confirm that the title has the word “Wikipedia” in it.
* Print the entire HTML of this page using the `page_source` property.
* Fetch an element through its CSS ID from the current web page (Wikipedia).
* Fetch the search bar component from the page using its CSS ID and then send the string "ASD" in this input field using the `send_keys()` function.
* Fetch an element through the CSS class from the current web page (Wikipedia).
* Fetch the search button from this page using its CSS class and then use the click event to execute the search query using the `click()` function.
#### 4. Switch to New Page
* After the click event, the WebDriver will open the following new page `https://en.wikipedia.org/wiki/ASD`, which shows all the search results. Use the `window_handles` statement to select any window.
* Use the `switch_to` function to switch to the selected window.
* Switch the WebDriver instance (`wd`) to this new window.
* Check if the new window contains the "ASD - Wikipedia" string in the title by using the assertion statement.
#### 5. Fetch Elements
* Fetch the link text of the string "Adaptive software development" from this webpage.
* Click and switch the WebDriver instance to this link.
* Using the assertion technique, check if the new WebDriver instance contains the string "Adaptive software development - Wikipedia" in the title.
* Fetch the entire text above the “References” heading from this page, which is defined in multiple `<p>...</p>` tags. Fetch all the elements into an array p_tags using these tag values.
* Extract the text from every element of the array `p_tags`, and append the text in a string variable `text_lines`.
* Wikipedia uses a citation format with the superscript numbers referencing the source mentioned under the “References” heading. Import the regex library and use it to remove these citations from the text and print clean text on the terminal.
* Fetch all the hyperlinks that occur inside the `<p>...</p>` tags using nested CSS selectors.
* Create a Python dictionary with hyperlink texts as keys and the URL they point to as values.
* Print this dictionary on the terminal using the `get_attribute` method to fetch the URLs of the hyperlinks.
### Conclusion
This project showcases how to use Selenium to scrape data from a website. It covers various Selenium commands and events to automate the processes on the website and how to clean the text data using regex library. 