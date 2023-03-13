from selenium import webdriver
from selenium.webdriver.chrome.service import Service
from selenium.webdriver.common.by import By

options= webdriver.ChromeOptions()
options.add_experimental_option("detach", True)

serv_obj = Service("C:\Drivers\chromedriver_win32\chromedriver.exe")

driver = webdriver.Chrome(options=options,service=serv_obj)

driver.get("https://demoqa.com/login")
driver.maximize_window()

driver.find_element(By.ID,"userName").send_keys("dshirke")
driver.find_element(By.ID,"password").send_keys("12345")
driver.find_element(By.XPATH, "//button[@id='login']").click()

if driver.find_element(By.XPATH, "/html/body/div[2]/div/div/div[2]/div[2]/div[2]/form/div[5]/div/p").is_displayed():
    print("Test Passed")

else:
    print("Failed")

