# node-lecture-simple-crud 
Simple crud Demo (node + koa2 + Mongodb)

Deploy applications on Tencent Cloud

## Quickly started
Use Linux `ubuntu` system

## Project structure
```
node-lecture-simple-crud/
├── README.md
├── app.js
├── bin
│   └── www
├── package-lock.json
├── package.json
├── public
│   ├── async.js
│   └── stylesheets
│       └── style.css
├── routes
│   ├── index.js
│   └── users.js
├── schema
│   └── index.js
└── views
    ├── detail.jade
    ├── error.jade
    ├── index.jade
    └── layout.jade
```

## Install
SSH into the server and perform the following installation

**Step1 - Install Node.js**
``` bash
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -    
```
``` bash
sudo apt-get install -y nodejs
```

**Step2 - Install MongoDB**
``` bash
# Import the public key used by the package management system. 
wget -qO - https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add - 

# Create a list file for MongoDB.
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list 

# Reload local package database. 
sudo apt-get update 

# Install the MongoDB packages.
sudo apt-get install -y mongodb-org
```

**Step3 - Start MongoDB**
``` bash
service mongod start
```

**Step4 - Clone Project**
``` bash
# /home/www
git clone https://github.com/sonic0828/node-lecture-simple-crud 

# install Project
cd node-lecture-simple-crud
npm install
```

**Step5 - Install PM2**
``` bash
npm install pm2 -g
```

## Start project
**Running at foreground**
``` bash
npm start
```

**Running at background(start whith pm2)**
``` bash
npm run prd
```

## Browser open
http://127.0.0.1:3030

Enjoy~