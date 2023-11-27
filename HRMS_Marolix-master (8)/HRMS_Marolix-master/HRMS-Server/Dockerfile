FROM python:3.8-slim
RUN apt-get update && apt-get install -y build-essential
RUN apt-get install -y libpq-dev
WORKDIR /app
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt
COPY . /app/
ENV DATABASE_NAME='HRMS'
ENV DATABASE_USER='devuser'
ENV DATABASE_PASSWORD='Devuser#123'
ENV DATABASE_HOST='216.48.191.120'
ENV DATABASE_PORT='5432'
ENV mailto:email_host_user='nihar@marolix.com'
ENV EMAIL_HOST_PASSWORD='C6050425D5DE4D829132626A42EF01D034D0'
ENV SECRET_KEY='django-insecure-#cedo6k@mkcoy%!r2$wy$8h-(9x&ev+v%tvx+-k-o%)2jt$fb^'
ENV EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
ENV EMAIL_HOST = 'smtp.elasticemail.com'
ENV EMAIL_PORT=25
ENV EMAIL_USE_TLS=True
ENV EMAIL_USE_SSL=False
ENV email_host_user='nihar@marolix.com'
ENV DEFAULT_FROM_EMAIL = 'mailto:nihar@marolix.com'
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
