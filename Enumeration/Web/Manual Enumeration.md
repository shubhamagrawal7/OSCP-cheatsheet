# Manual Web Enumeration

Manual web enumeration involves manually checking a web application for vulnerabilities and misconfigurations. Here are some useful techniques to use when manually enumerating a web application.

## Check robots.txt

The robots.txt file is used by web crawlers to determine which parts of a website should not be crawled or indexed. It is often used by web developers to exclude sensitive or private information from being indexed by search engines.

**Example: To check the robots.txt file of a web application, simply add `/robots.txt` to the end of the URL. For example, if the URL of the web application is `https://example.com`, then the URL to check the robots.txt file would be `https://example.com/robots.txt`.**

## Check for comments in the source code

Comments in the source code of a web application can provide valuable information about the application's structure and functionality. They can also reveal potential vulnerabilities or misconfigurations.

**Example: To check for comments in the source code, simply view the page source by right-clicking on the page and selecting "View Page Source" or "View Source". Look for comments in HTML, JavaScript, or CSS files.**

## Check open directory listings

An open directory listing occurs when a web server is configured to show the contents of a directory rather than a specific web page. This can reveal sensitive information about the application's file structure and can provide attackers with valuable information about potential vulnerabilities.

**Example: To check for open directory listings, simply navigate to the root directory of the web application and see if a directory listing is displayed. For example, if the URL of the web application is `https://example.com/images/`, then navigate to `https://example.com/images/` and check if a directory listing is displayed.**

## Checking Cookies

During website enumeration, checking cookies can provide valuable information about the site's functionality, authentication mechanisms, and potential vulnerabilities. Here are some techniques for checking cookies:

* **Manipulate Cookies**
  - Use a browser extension like EditThisCookie or Cookie Editor to modify cookie values.
  - Experiment with modifying cookie values to see if it affects the website's behavior.
  - For example, you can try changing authentication-related cookies or session cookies to test for potential vulnerabilities or bypass authentication mechanisms.

* **Decode/Decrypt Cookies**
  - If the cookies are encoded or encrypted, use appropriate techniques to decode or decrypt them.
  - Common encoding schemes include Base64 and URL encoding.
  - If encryption is involved, analyze the encryption algorithm and key management to attempt decryption.
  - Tools like CyberChef or custom scripts can assist in decoding or decrypting cookies.
