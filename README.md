# YandexWebDriver

## Intro

YandexDriver is a WebDriver implementation derived from [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/) and adapted by Yandex that enables programmatic automation of Yandex.Browser. It is a part of the [Selenium](http://code.google.com/p/selenium) project.

## Binaries

Binaries are available under [the releases tab](https://github.com/yandex/YandexDriver/releases).

## Desktop usage
1. Download binary file for your platform.
2. Example code for python on Windows
```python
from selenium import webdriver
from selenium.webdriver.chrome.service import Service

service = Service(executable_path=r"/path/to/yandexdriver.exe") # Path to the Yandex Driver

options = webdriver.ChromeOptions()

driver = webdriver.Chrome(service=service, options=options)
driver.get("https://yandex.ru")
driver.quit()
```



## Android usage
1. Download binary file for host.
2. Attach android device with Yandex.Browser to host. Check by running adb devices.
3. Enable USB Web-pages debugging in Settings in Yandex.Browser.
4. Example code for python on Windows host
```python
from selenium import webdriver
options = webdriver.ChromeOptions()

binary_yandex_driver_file = 'yandexdriver.exe'     # path to YandexDriver
yandex_browser_package_name = 'com.yandex.browser' # Release version of Yandex.Browser

options.add_experimental_option('androidPackage', yandex_browser_package_name)
driver = webdriver.Chrome(binary_yandex_driver_file, options=options)
driver.get('https://yandex.ru')
driver.quit()
```
  
