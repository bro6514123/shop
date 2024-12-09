FROM python:3.9

# Відкрити порт 8000
EXPOSE 8000

# Встановити робочу директорію
WORKDIR /backend

# Скопіювати залежності та встановити їх
COPY requirements.txt . 
RUN pip install --no-cache-dir -r requirements.txt

# Скопіювати весь проект у контейнер
COPY ./src ./src

# Запускати сервер Django
CMD ["python", "src/manage.py", "runserver", "0.0.0.0:8000"]
