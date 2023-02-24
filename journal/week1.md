# Week 1 — App Containerization
## Containerize Backend

### Run python
```sh
cd backend-flask
export FRONTEND_URL="*"
export BACKEND_URL="*"
python3 -m flask run --host=0.0.0.0 --port=4567
cd ..
```
 - Make sure to unlock the port in port tab
 - open the link for 4567 in your browser
 - append to the url to /api/activities/home
 - you should get back json

### Build/Add docker file
Create a file : ``backend-flask/Dockerfile``

```sh
FROM python:3.10-slim-buster

WORKDIR /backend-flask

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]

```

### Build Container
```
docker build -t  backend-flask ./backend-flask
```

### Run Container

```
docker run --rm -p 4567:4567 -it -e FRONTEND_URL='*' -e BACKEND_URL='*' backend-flask
```

## Frontend Containerize
Open the frontend-react-js in cmd terminal and run 
```sh
npm install
``
