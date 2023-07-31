# Flask with React App

create a folder `flask-server` which contain our flask app

    touch server.py

then create a front end react app - `client`

    npx create-react-app client

Create venv for python app and activate

    python3 -m venv svenv
    source svenv/bin/activate

Install flask in venv

    pip3 install Flask

<br>

### setting react app

#### unnecessary files in react

1. App.test.js
2. index.css
3. logo.svg
4. remove import of index.css in index.js

Configure the proxy in `package.json` to connect the backend to the front end for that insert the following line in `package.json`.

    "proxy": "http://127.0.0.1:5000"

we add the backend server in `proxy`. So that we can tell react which port our backend is running and so that we can make relative request.

Then we can add code on App.js

We use `useEffect` to fetch the data from the backend url, we are going to put that response into json and whatever the data that is inside of the json, we are going to set that data into data variable `setData`.
