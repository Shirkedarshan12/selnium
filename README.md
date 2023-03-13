from selenium import webdriver
from selenium.webdriver.common.by import By

def test_selenium_demo():
    options= webdriver.ChromeOptions()
    options.add_experimental_option("detach", True)

    driver =webdriver.Chrome(options=options)
    driver.get("https://www.facebook.com")
    element=driver.find_elements(By.ID,"email")
    element.clear()
    element.send_keys("Test@gmail.com")

    element_pass = driver.find_element(By.ID, "pass")
    element_pass.clear()
    element_pass.send_keys("Password")

    login_button_element= driver.find_element(By.NAME, "login")
    login_button_element.click()

test_selenium_demo()
