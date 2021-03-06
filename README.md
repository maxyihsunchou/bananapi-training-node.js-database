# BananaPi M2+ Training Nov. 5

## Introduction
本 Project 主要是以 Node.js + MongoDB with APi design 的部分。

## How to do?

### Step 1 - 抓下本專案
開啟您指定的路徑下終端機，在終端機內輸入
（以下全部步驟皆在 終端機 內部執行）
<br>
```git clone https://github.com/maxyihsunchou/bananapi-training-node.js-database.git```

### Step 2 - 進入專案資料夾
```cd bananapi-training-node.js-database```

### Step 3 - 安裝 Node.js
#### 安裝 Node.js 與 NPM

```sudo apt-get update```

#### Node.js

```sudo apt-get install nodejs```

#### NPM

```sudo apt-get install npm```

#### Step 4 - Install and Config MongoDB

```sudo apt-get install -y mongodb```

### Config MongoDB

```sudo vim /lib/systemd/system/mongod.service```

在此檔案內貼上以下文字

```
[Unit]
Description=High-performance, schema-free document-oriented database
After=network.target
Documentation=https://docs.mongodb.org/manual

[Service]
User=mongodb
Group=mongodb
ExecStart=/usr/bin/mongod --quiet --config /etc/mongod.conf

[Install]
WantedBy=multi-user.target
```

按ESC 之後以 ```:wq``` 儲存變更

### Step 5 - 請確任全部動作安裝都執行過

在目錄裡下輸入
<br>
```sudo service mongod start```
<br>
開啟 MongoDB 的服務
<br>
與 伺服器
<br>
```npm start```
<br>
### Step 6 - 測試看看是否成功！
在 Google Chrome 的網址列中輸入
```
http://localhost:3000/
```
如果看到 Welcome to Express 就是成功了。

## Other information
### 新增 資料路徑
```
localhost:3000/control/article/add/
```

### Api 部分
Read all of data
---
```
localhost:3000/api/article/
```
Read a data with ID
---
```
localhost:3000/api/article/<your_id_here>
```
# All Done!
