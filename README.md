# selnium

from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.common.by import By

serv_obj = Service("C:\Drivers\chromedriver_win32\chromedriver.exe")
options= webdriver.ChromeOptions()
options.add_experimental_option("detach", True)

driver = webdriver.Chrome(options=options,service=serv_obj)

driver.get ("https://www.facebook.com/")

driver.find_elements(By.NAME,"email").send_keys("dshirke802@gmail.com")
driver.find_elements(By.ID,"pass").send_keys("12345")
driver.find_element(By.NAME, "login").click()
