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
# childs=driver.find_elements(By.XPATH, "//a[contains(text(), 'Indian Infotech')]/ancestor::tr/child::td")
# print(len(childs))

# Ancestor
# text_msg=driver.find_element(By.XPATH, "//a[contains(text(), 'Indian Infotech')]/ancestor::tr").text    # It will print text of all child node (tr= table row & td = table data)
# print(text_msg)


# Decendant
# decendant=driver.find_elements(By.XPATH, "//a[contains(text(), 'Indian Infotech')]/ancestor::tr/descendant::*")
# print(len(decendant))   #7

# Following
# followings=driver.find_elements(By.XPATH, "//a[contains(text(), 'Indian Infotech')]/ancestor::tr/following::*")
# print(len(followings))   #13764

# Following sibling
# followingsSiblings=driver.find_elements(By.XPATH, "//a[contains(text(), 'Indian Infotech')]/ancestor::tr/following-sibling::*")
# print(len(followingsSiblings))   #1698


# Precedings
# preceding=driver.find_elements(By.XPATH, "//a[contains(text(), 'Indian Infotech')]/ancestor::tr/preceding::*")
# print(len(preceding))    #301

# Precedings following
# precedingSibling=driver.find_elements(By.XPATH, "//a[contains(text(), 'Indian Infotech')]/ancestor::tr/preceding-sibling::*")
# print(len(precedingSibling))    #15



