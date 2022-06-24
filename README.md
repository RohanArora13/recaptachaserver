
# Google Recapcha v2 Solver Server

a repo made to host on heroku (or any platform).helps solve recapcha using images and yolo3 model


[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/tterb/atomic-design-ui/blob/master/LICENSEs)

[![Herko](https://img.shields.io/badge/heroku-pass-green)](https://heroku.com/login)


## Please reffer

| Repo | Link |
| ------ | ------ |
| byerecaptcha| https://github.com/DedInc/byerecaptcha |
| solverecaptchas | https://github.com/embium/solverecaptchas |

## Usecase


```python
from selenium import webdriver
from selenium_utilities import getChromeDriver
from byerecaptcha import solveRecaptcha

options = webdriver.ChromeOptions()
options.add_argument('--lang=en-US') #need for recaptcha be in english

driver = webdriver.Chrome(executable_path=getChromeDriver(), chrome_options=options)
driver.get('https://www.google.com/recaptcha/api2/demo')
solveRecaptcha(driver) #FOR PREDICTION ON YOUR PC

solveRecaptcha(driver, "https://yourserver.heroku.com") #FOR PREDICTION IN YOUR SERVER (check server.py)
```

## Tech Stack

**Client:** Python, selenium, byerecaptcha

**Server:** python, flask, numpy
