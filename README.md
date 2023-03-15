from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.common.by import By


options= webdriver.ChromeOptions()
options.add_experimental_option("detach", True)

serv_obj = Service("C:\Drivers\chromedriver_win32\chromedriver.exe")

driver = webdriver.Chrome(options=options,service=serv_obj)

driver.get ("https://money.rediff.com/gainers")
driver.maximize_window()


# self
# text_msg=driver.find_element(By.XPATH, "//a[contains(text(), 'Indian Infotech')]/self::a").text
# print(text_msg)   #India Infotech


# parent
# text_msg=driver.find_element(By.XPATH, "//a[contains(text(), 'Indian Infotech')]/parent::td").text
# print(text_msg)   #India Infotech


# child
childs=driver.find_elements(By.XPATH, "//a[contains(text(), 'Indian Infotech')]/ancestor::tr/child::td")
print(len(childs))


