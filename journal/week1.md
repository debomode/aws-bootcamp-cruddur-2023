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

