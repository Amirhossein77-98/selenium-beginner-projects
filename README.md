# Selenium Web Scraper

This project is a Jupyter Notebook that uses Selenium to scrape text from a website. It is designed to work with Chrome version 125.0.6422.14 (Official Build) beta (64-bit).

## Prerequisites

Before running the notebook, make sure you have the following installed:

- Python 3.x
- Jupyter Notebook
- Google Chrome Browser (version 125.0.6422.14 beta)
- ChromeDriver (compatible with Chrome version 125.0.6422.14)

## Installation

1. Clone the repository or download the source code.
2. Install the required Python packages by running the following command: `pip install -r requirements.txt`

3. Download the compatible ChromeDriver for your operating system from the official website: [ChromeDriver Downloads](https://sites.google.com/a/chromium.org/chromedriver/downloads).
4. Extract the ChromeDriver executable and place it in the project directory or another directory included in your system's PATH.

## Usage
 
1. Open a terminal or command prompt, navigate to the project directory, and start the Jupyter Notebook server: `jupyter notebook`
2. In the Jupyter Notebook interface, navigate to the notebook file (e.g., `scraper.ipynb`).
3. In the notebook, update the `chrome_bin_path` variable with the correct path to your Google Chrome binary. For example, on Windows, it might look like this:

```chrome_bin_path = r"C:\Program Files\Google\Chrome Beta\Application\chrome.exe"```

Run the notebook cells in order.

The notebook will launch the Chrome browser, navigate to the specified website (https://soft98.ir in the provided example), wait for an element with the class name "nbdvlk" to be present, and print its text content.

## Customization

You can modify the notebook to scrape data from different websites or look for different elements by adjusting the following code:
`driver.get("https://soft98.ir")  # Replace with the desired URL`
`element = wait.until(EC.presence_of_element_located((By.CLASS_NAME, "nbdvlk")))  # Replace the locator strategy and value`

Additionally, you can adjust the timeout value for the WebDriverWait instance by modifying the second argument: `wait = WebDriverWait(driver, 10)  # Wait for up to 10 seconds`

## Troubleshooting

If you encounter any issues while running the notebook, make sure that:

- The Chrome browser version matches the specified version in the notebook.
- The ChromeDriver version is compatible with the Chrome browser version.
- The paths to the Chrome binary and ChromeDriver executable are correct.