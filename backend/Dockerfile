FROM python:3.11.15-alpine3.22

#WORKDIR app/

COPY requirements.txt .

#WORKDIR app/

RUN pip install -r requirements.txt

#WORKDIR app/
COPY app/ app/

#ENTRYPOINT ["python","-m", "app.main"]
ENTRYPOINT ["uvicorn"]
CMD ["app.main:app", "--host", "0.0.0.0", "--port", "8000"]
