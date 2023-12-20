FROM python:3.9

WORKDIR stocks_products

COPY . .

RUN pip3 install --no-cache-dir --upgrade -r requirements.txt

ENV MY_ENV=netology

RUN python manage.py migrate

EXPOSE 6060

CMD ["gunicorn", "-b", "0.0.0.0:8001", "stocks_products.wsgi:application"]