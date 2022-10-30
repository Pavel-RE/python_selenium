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
