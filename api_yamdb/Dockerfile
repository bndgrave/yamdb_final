FROM python:3.9.5-slim

WORKDIR /app
COPY ./api_yamdb/requirements.txt .
COPY . .

RUN python -m pip install --upgrade pip
RUN pip3 install -r requirements.txt --no-cache-dir

WORKDIR /app/api_yamdb
CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ] 
