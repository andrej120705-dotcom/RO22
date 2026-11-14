echo off
chcp 65001 > nul
echo =======================================================
echo   Запуск веб-додатка розрахунку зворотного осмосу
echo =======================================================
echo.
set "PYPATH=C:\Users\ASUS\AppData\Local\Programs\Python\Python311\python.exe"
if exist "%PYPATH%" (
    echo Запускаємо через Python 3.11...
    "%PYPATH%" -m streamlit run app.py
) else (
    echo Запускаємо через системний streamlit...
    streamlit run app.py
)
pause
