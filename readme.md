

# LinkedIn Accept Automation

---

## **Description**

LinkedIn Accept Automation is a Python-based automation tool designed to streamline the process of accepting LinkedIn connection invitations. This script automates the login process and accepts all pending invitations on your LinkedIn network.

---

## **Author**

- **Name**: Naufal Rizqullah F  
- **Contact**: [naufalrf4@gmail.com](mailto:naufalrf4@gmail.com)  

---

## **Requirements**

Before running the script, ensure you have the following installed:

1. **Python 3.9 or higher**: Download from [python.org](https://www.python.org/downloads/).
2. **Browser**:
   - **Google Chrome**: Download from [google.com/chrome](https://www.google.com/chrome/).
   - **Microsoft Edge**: Download from [microsoft.com/edge](https://www.microsoft.com/edge).
3. **WebDriver**:
   - **ChromeDriver**: Download the version matching your Chrome browser from [ChromeDriver](https://sites.google.com/chromium.org/driver/).
   - **EdgeDriver**: Download the version matching your Edge browser from [EdgeDriver](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/).
4. **Environment Variables**: Create a `.env` file to store your LinkedIn credentials and WebDriver path.

---

## **Environment Settings**

1. Copy the `.env.example` file to `.env`:
   ```bash
   cp .env.example .env
   ```
2. Open the `.env` file and update the following variables:
   ```env
   LINKEDIN_EMAIL=your_linkedin_email
   LINKEDIN_PASSWORD=your_linkedin_password
   CHROMEDRIVER_PATH=/path/to/chromedriver  # Uncomment and set if using Chrome
   # EDGEDRIVER_PATH=/path/to/edgedriver    # Uncomment and set if using Edge
   ```
   Replace `your_linkedin_email`, `your_linkedin_password`, and the driver paths with your actual credentials and driver paths.

---

## **Setup**

1. Ensure the `.env` file is correctly configured.
2. Choose your preferred browser:
   - **For Chrome**: Uncomment the Chrome driver initialization in the script.
   - **For Edge**: Uncomment the Edge driver initialization in the script.
3. Verify that the WebDriver is installed and the path is correct in the `.env` file.

---

## **Install Requirements**

1. Set up a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

---

## **Tutorial: How to Use the Automation**

1. **Select Browser**: Uncomment the driver initialization for your chosen browser in the script.
2. **Login**: The script will automatically log in to your LinkedIn account using the credentials provided in the `.env` file.
3. **Accept Invitations**: The script navigates to the invitations page and accepts all pending connection requests.

---

## **Troubleshooting**

- **Browser Selection**: Ensure that you have uncommented the correct driver initialization for your chosen browser.
- **WebDriver Issues**: Ensure the correct version of the WebDriver is installed and matches your browser version.
- **Login Failures**: Double-check your `.env` file to ensure the email and password are correct.
- **Timeout Errors**: If the script times out, ensure your internet connection is stable and LinkedIn is accessible.

---

## **Example `.env` file:**

```env
LINKEDIN_EMAIL=your_linkedin_email
LINKEDIN_PASSWORD=your_linkedin_password
CHROMEDRIVER_PATH=/path/to/chromedriver  # Uncomment and set if using Chrome
# EDGEDRIVER_PATH=/path/to/edgedriver    # Uncomment and set if using Edge
```

---

## **Updated Script Comments:**

```python
# Using ChromeDriver
service = ChromeService(chrome_driver_path)
options = webdriver.ChromeOptions()
options.add_argument("--start-maximized")
try:
    driver = webdriver.Chrome(service=service, options=options)
    print("ChromeDriver started successfully.")
except WebDriverException as e:
    print(f"Error starting ChromeDriver: {e}")
    raise

# Using EdgeDriver
# service = EdgeService(edge_driver_path)
# options = webdriver.EdgeOptions()
# options.add_argument("--start-maximized")
# try:
#     driver = webdriver.Edge(service=service, options=options)
#     print("EdgeDriver started successfully.")
# except WebDriverException as e:
#     print(f"Error starting EdgeDriver: {e}")
#     raise
```
