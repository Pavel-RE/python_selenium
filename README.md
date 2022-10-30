автотесты на selenium web driver


# Создать виртуальное окружение:
**Важно: выполнять в командной строке в корне проекта**

1) Создаем виртуальное окружение (возможно не python, а python3)  
**`python -m venv env`**

2) Активируем окружение  
**`.\env\Scripts\Activate.ps1`** # команда для Windows  
**`source env/bin/activate`**    # команда для Mac и Linux  

3) Деактивация окружения  
**`deactivate`**


# Установка модулей:
**`pip install pytest`**  
**`pip install selenium`**  
**`pip install webdriver_manager`**  
**`pip install allure-pytest`**



# Запуск тестов:
1) Из командной строки: 
**`pytest test_product_view_sku`**
2) Через VS Code. Пример файла с настройками:  
```JSON
{  
    "python.testing.pytestArgs": [ 
        "tests",
        "--alluredir=my_allure_results"   # настройка для сохранения отчетов  
        ],
    "python.testing.unittestEnabled": false, 
    "python.testing.pytestEnabled": true 
}
```
# Запустить дашборд с отчетами:
1. Установить Allure Report:  
**`brew install allure`**    # команда для Mac  
**`sudo apt-add-repository ppa:qameta/allure`**   
**`sudo apt-get update`**   
**`sudo apt-get install allure`** # команды для Linux (Debian)    
Для Windows нужно скачать
  
- В Windows находим в каталоге *allure\bin* файл *allure.bat* и запускаем на выполнение
- На Linux/Mac выполняем файл рядом *./allure*

2. Добавить каталог для хранения отчетов allure:  
**`mkdir my_allure_results`**  

3. Выполнить несколько тестов, которые есть в проекте. 

4. Запустить сервер отчетов командой:  
**`cd <путь до каталог allure\bin>`** 
**`.\allure.bat`** 
**`.\allure serve <путь до каталога с результатами>`** 

**Пример итогового отчета:**
![](http://reshetniak.ru/img2/allure_report.png)
