Operating System Final Project
=======
# Introduction
The project is aimed to solve a typical process synchronization called "Sleeping Barber problem". While the problem can be solved by using some basic synchronization primitives , we add more complexity on it. We build a web application to visualize the result, and make it possible for user to interact with the application through webpages.
They can configure threads and dispatch a customer manually.
Through building the web application, we not only used synchronization also learned RPC and IPC stuffs, which is definitly helpful. The communication between main process and python process is through writing and reading via standard stream. We also use Websocket for realtime update barbershop result on webpage. The part is almost done by an Javascript package called `socket.io`, which has a clear interface and good documentation.
# Installation Guide
## Prerequisite
Please make sure you have below programs installed.
1. NPM and [Node.js](https://nodejs.org/en/)(version 8)
2. [Python3](https://www.python.org/downloads/) (we use python3.6)

## Set up local development environment
1. Make a directory and setup a python virtual environment.
```shell
mkdir <your-directory-name>
cd <your-directory-name>

// I use virtualenv. This is not a requirement really. Just make
// sure you dont mess with your local environment.

virtualenv env
source env/bin/activate
```
2. Clone the project.
```
git clone git@github.com:Honesty1997/OS-2018-Fall-Final-Project.git

// or use https
git clone https://github.com/Honesty1997/OS-2018-Fall-Final-Project.git
```

3. (optional)Change the project name since it is too long.
```
mv OS-2018-Fall-Final-Project <your-desired-name>
```
4. cd <your-desired-name>
5. Check you python version. We use python3 to execute our python script, so please make sure your python version is up to date.
```
python -V
# Python 3.6.6
```
6. install all python and node dependencies.
```
npm install
pip install -r requirements.txt
```

## Start server
1. If you just want to debug python file. Use
```
python3 main.py
```
2. Watch front-end and back-end file.
```
npm run watch
```
3. Start dev server
```
npm run dev-start
```
4. Build the project and run in production mode.
```
npm run build
npm start
```
