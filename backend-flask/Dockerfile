FROM python:3.10-slim-buster

#don't need to run the next cmd the workdir step will create a directory if it doesn't exist.
RUN mkdir -p /backend-flask

WORKDIR /backend-flask

COPY requirements.txt requirements.txt

RUN pip3 install -r requirements.txt

#copies everything from source to destination. First period denotes source  second period denotes Container
COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}

CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]

