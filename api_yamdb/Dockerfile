FROM python:3.9.5-slim
COPY . /app
WORKDIR /app
RUN pip3 install -r requirements.txt --no-cache-dir
CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ] 
