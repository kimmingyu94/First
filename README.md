# First
## github used
### 파일 실행
```
gcc -o run test.c
```
### apt 업데이트
```
sudo apt update
```
### github 불러오기
```
git clone https://github.com/sim0297/project name
cd project 
```
#### file remove
```
sudo rm 폴더명/ -rf
```
### 변경사항 깃허브에 적용
```
git add .
```
### 주석달듯이 변경사항 적용하기
```
git commit -m upload
```
### github config 
```
git config --global user.email "email"
git config --global user.name "user name"
```
py### github 업로드
```
git push
```
### git push error vim
```
git pull
```
이후 git add . 이후부터 다시

![gitpull](https://user-images.githubusercontent.com/66464064/83858723-e38ec780-a757-11ea-9974-d082f43b8e07.JPG)
-----------------------------------
### 고정IP
```
sudo apt-get install vim (빔설치)
vim /etc/dhcpcd.conf
```
### firewall
```
sudo ufw allow (port)
sudo ufw enable
sudo ufw status
sudo ufw disable
```
### vim editor setting
```
vim .vimrc
 set nu                              < line num
 set cindent                         < C language indent
 set ts=4                            < python tapsize 4
 set softtabstop=4                   < 
 set bg=dark                         <
 set expandtab
 let python_version_2 = 1
 let python_highlight_all = 1
 filetype indent plugin on
 if has("syntax")                    < syntax on
     syntax on
 endif
```
-----------------------------------

### DHT11 sensor pinmap(DHT11)
>VCC = 5V(4) | 
>GND = ground(6) | 
>DOUT = GPIO4(7)

# DHT11 sensor install
```
git clone https://github.com/adafruit/Adafruit_Python_DHT.git
cd Adafruit_Python_DHT
sudo python setup.py install
cd Adafruit_Python_DHT/examples
```
- run
```
python AdafruitDHT.py 11 4
or
python simpletest.py
```

# influxDB installation
## 1. Repository GPG key 
```
curl -sL https://repos.influxdata.com/influxdb.key | sudo apt-key add -
```
## 2. Repository add
```
echo "deb https://repos.influxdata.com/debian stretch stable" | sudo tee /etc/apt/sources.list.d/influxdb.list
```
## 3. Program Install
```
sudo apt update
sudo apt install influxdb
```
## 4. Run
``` 
sudo service influxdb start
influx
```
## 5. DB create
```
>create database 데이터베이스이름
```
#### 5-1. 확인
```
show databases
```
#### 5-2. DB 나가기
```
exit
```

# Grafana Installation
## 1. Repository GPG key
```
curl https://bintray.com/user/downloadSubjectPublicKey?username=bintray | sudo apt-key add -
```
## 2. Repository add
```
echo "deb https://dl.bintray.com/fg2it/deb stretch main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
```
## 3. Install
```
sudo apt update
sudo apt install grafana
```
## 4. Run
```
sudo service grafana-server start
```
## influxdb import with python
```
sudo pip install influxdb
```

