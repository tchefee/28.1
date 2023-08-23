#Тестирование интерфейса авторизации в Личном Кабинете Ростелеком
https://b2c.passport.rt.ru

#Тест-кейсы и баг-репорт:
https://docs.google.com/document/d/1mZi8GpWUvpGD4za7kOgDWTfVTktWB8ks1qeMgHKmSYk/edit

#При тестировании применялись следующие методики: 
    <br>- пограничные значения, 
    <br>- эквивалентное разделение, 
    <br>- предугадывание ошибок, 
    <br>- исследовательское тестирование,
    <br>- параметризация тестов.

#Проект выполнен на Python 3.9, использовались библиотеки Pytest и Selenium

#Окружение: Windows 10, Google Chrome v.116.0.5845.111 + chromedriver.
<br><br>#File list:
    <br>- conftest.py содержит весь необходимый код для отлова неудачных тестовых случаев и создания скриншота страницы в случае, если какой-либо тестовый пример не сработает.
    <br>- pages/base.py содержит реализацию шаблона PageObject для Python.
    <br>- pages/auth_locators.py локаторы страницы авторизации для работы с автотестами.
    <br>- pages/elements.py содержит вспомогательный класс для определения веб-элементов на веб-страницах.
    <br>- test_rostelecom.py содержит тесты для ЛК Ростелеком
    <br>- settings.py содержит тестовые данные для тестов

#Запуск тестов:
    <br>- Установить требования: pip install -r requirements.txt
    <br>- Загрузить Selenium WebDriver с https://chromedriver.chromium.org/downloads

#Все тесты разом командой из терминала: 
    <br>python -m pytest -v --driver Chrome --driver-path C:/Projects/chromedriver.exe
    <br>где C:/Projects/chromedriver.exe путь до chromedriver.exe

#Запустить каждый тест по отдельности:
    <br>pytest test_rostelecom.py::test_wrong --driver Chrome --driver-path C:/Projects/chromedriver.exe
    <br>где test_wrong название теста, который хотим запустить.