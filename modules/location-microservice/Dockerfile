FROM python:3.7-alpine

WORKDIR .

COPY . .
RUN pip install -r requirements.txt

EXPOSE 5005

COPY . .
CMD ["python", "grpc_server.py"]