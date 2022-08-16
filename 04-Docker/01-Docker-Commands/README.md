```
1949  cd 04-Docker/
 1950  ls
 1951  cd 00-Setup/
 1952  ls
 1953  cat install-docker.sh
 1954  ls
 1955  ./install-docker.sh
 1956  docker version
 1957  docker images
 1958  docker ps -qa
 1959  docker rm $(docker ps -qa)
 1960  docker images
 1961  docker images -q
 1962  docker rmi $(docker images -q)
 1963  docker rmi $(docker images -q)  --force
 1964  docker images
 1965  docker ps
 1966  docker ps -a
 1967  docker run busybox echo "Welcome to the world of Docker"
 1968  docker container ls
 1969  docker container ls -a
 1970  docker run busybox echo "Welcome to the world of Docker"
 1971  docker container ls -a
 1972  docker run busybox echo "Test - 1"
 1973  docker run busybox echo "Test - 2"
 1974  docker container ls -a
 1976  docker run busybox lsop
 1977  docker container ls -a
 1978  docker container ls
 1979  docker container ls -a
```


```
1993  docker images
 1994  docker pull ubuntu
 1995  docker images
 1996  docker pull ubuntu:16.04
 1997  docker ps
 1998  docker images
 1999  docker pull amitvashist7/k8s-tiny-web
 2000  docker images
```
```
 1032  docker run -it ubuntu:16.04
 1033  docker ps
 1034  docker container ls
 1035  docker container ls -a
 1036  docker run -it ubuntu
 1037  history
 1038  docker run -it --name test-1 ubuntu
 1039  docker ps
 1040  docker ps -a
 1041  docker run -it --name test-1 ubuntu
 1042  docker run -d --name test-2 ubuntu
 1043  docker ps -a
 1044  docker run -itd --name test-3 ubuntu
 1045  docker ps -a
 1046  docker ps
 1047  docker stop test-3
 1048  docker ps
 1049  docker ps -a
 1050  docker start test-3
 1051  docker ps
 1052  docker attach test-3
 1053  docker ps
 1054  docker ps -a
 1055  docker start test-3
 1056  docker ps -a
 1057  docker attach test-3
 1058  docker ps
 1059  docker attach test-3
 1060  ls
 1061  docker ps
 1062  ls
 1063  docker ps -a
 1064  docker run -itd --name test-4 ubuntu
 1065  docker run -itd --name test-5 ubuntu
 1066  docker run -itd --name test-6 ubuntu
 1067  docker ps
 1068  docker inspect test-3
 1069  docker ps
 1070  docker ps -a
 1071  docker ps
 1072  docker ps -q
 1073  docker inspect $(docker ps -q)
 1074  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -q)
 1075  docker ps
 1076  docker ps -a
 1077  docker ps -aq
 1078  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
 1079  docker start test-2
 1080  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
 1081  docker ps
 1082  docker kill $(docker ps -q)
 1083  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
 1084  docker rm $(docker ps -aq)
 1085  docker ps -a
 1086  docker images
 1087  docker rmi busybox
 1088  docker images

```




```
cker-Images
 1107  ls
 1108  cd 02-Docker-Images/
 1109  ls
 1110  mkdir apache/v1
 1111  mkdir apache/v1 -p
 1112  ls
 1113  cd apache/
 1114  ls
 1115  cd v1/
 1116  ls
 1117  vim Dockerfile
 1118  ls
 1119  docker ps -a
 1120  docker run -itd ubuntu:16.04
 1121  docker ps
 1122  ls
 1123  docker build -t myapache .
 1124  docker images
 1125  docker run -d --name test-apache-1 myapache
 1126  docker ps
 1127  docker inspect 0~test-apache-11~
 1128  docker inspect test-apache-1
 1129  docker ps
 1130  curl 172.17.0.3
 1131  history
 1132  ls
 1133  docker ps
 1134  docker run -d --name test-apache-2 myapache
 1135  docker run -d --name test-apache-3 myapache
 1136  docker ps
 1137  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
 1138  curl 172.17.0.3
 1139  curl 172.17.0.4
 1140  curl 172.17.0.5
 1141  curl 172.17.0.6
 1142  curl 172.17.0.2
```


```


```


```

 1167  cp -rf v1 v2
 1168  ;s
 1169  ls
 1170  cd v2/
 1171  ls
 1172  mv Dockerfile myapache-file
 1173  ls
 1174  vim myapache-file
 1175  s
 1176  ls
 1177  vim index.html
 1178  ls
 1179  docker build -t myapache .
 1180  ls
 1181  docker build -t myapache -f myapache-file .
 1182  docker images
 1183  docker run -d --name test-apache-4 myapache
 1184  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
 1185  curl 172.17.0.6
 1186  docker tag d3d23e5a87be myapache:v1
 1187  docker tag 027edfdd5ef2 myapache:v2
 1188  docker images
 1189  docker run -d --name test-apache-4 myapache:v1
 1190  docker run -d --name test-apache-5 myapache:v1
 1191  docker run -d --name test-apache-6 myapache:v2
 1192  docker ps
 1193  s
 1194  docker ps
 1195  curl -vv 172.17.0.6
 1196  s
 1197  cd ..
 1198  ls
 1199  cp -rf v2 v3
 1200  ls
 1201  cd v3/
 1202  ls
 1203  mv myapache-file Dockerfile
 1204  ls
 1205  vim index.html
 1206  ls
 1207  vim Dockerfile
 1208  ls
 1209  docker build -t myapache:v3  .
 1210  docker images
 1211  docker run -d --name test-apache-7 myapache:v3
 1212  docker ps
 1213  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
 1214  curl -vv 172.17.0.8
 1215  curl  172.17.0.8
 1216  curl  172.17.0.9
 1217  curl  172.17.0.9:80
 1218  cd ..
 1219  ls
 1220  cp -rf v3 v4
 1221  cd v4/
 1222  s
 1223  ls
 1224  vim Dockerfile
 1225  s
 1226  docker build -t myapache:v4  .
 1227  docker run -d --name test-apache-8 myapache:v4
 1228  docker ps
 1229  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
 1230  curl 172.17.0.10:3306
 1231  curl 172.17.0.10:8080
 1232  docker inspect e5fcc6c87a28
 1233  ls
 1234  cd ..
 1235  ls
 1236  cp -rf v4 v5
 1237  ls
 1238  cd v5/
 1239  ls
 1240  vim Dockerfile
 1241  ls
 1242  docker build -t myapache:v5  .
 1243  docker images
 1244  vim index.html
 1245  docker build -t myapache:v5  .
 1246  docker images
 1247  docker run -d --name test-apache-9 myapache:v5
 1248  curl 172.17.0.11
 1249  ls
 1250  cd ../../../
 1251  ls
 1252  cd ..
 1253  ls
 1254  docker images
 1255  docker push myapache:v5
 1256  docker login
 1257  docker logout
 1258  docker login
 1259  docker push myapache:v5
 1260  docker images
 1261  docker tag d1e615b4043d amitvashist7/devops-netmagic-08-aug-2022-myapache:v5
 1262  docker tag d1e615b4043d amitvashist7/devops-netmagic-08-aug-2022-myapache:latest
 1263  docker images
 1264  docker push amitvashist7/devops-netmagic-08-aug-2022-myapache
 1265  docker push amitvashist7/devops-netmagic-08-aug-2022-myapache:v5
 1266  docker tag c9134a18cded amitvashist7/devops-netmagic-08-aug-2022-myapache:v4
 1267  docker tag myapache:v3 amitvashist7/devops-netmagic-08-aug-2022-myapache:v3
 1268  docker tag myapache:v2 amitvashist7/devops-netmagic-08-aug-2022-myapache:v2
 1269  docker tag myapache:v1 amitvashist7/devops-netmagic-08-aug-2022-myapache:v1
 1270  docker images
 1271  docker push amitvashist7/devops-netmagic-08-aug-2022-myapache:v4
 1272  docker push amitvashist7/devops-netmagic-08-aug-2022-myapache:v3
 1273  docker push amitvashist7/devops-netmagic-08-aug-2022-myapache:v2
 1274  docker push amitvashist7/devops-netmagic-08-aug-2022-myapache:v1
 1275  docker images
 1276  docker images -q
 1277  docker rmi $(docker images -q)
 1278  docker kill $(docker ps -q)
 1279  docker rm $(docker ps -aq)
 1280  docker ps -a
 1281  docker rmi $(docker images -q)
 1282  docker rmi $(docker images -q) --force
 1283  docker images
 1284  ls
 1285  docker images
 1286  docker logout
 1287  docker run -d  --name test-1 amitvashist7/devops-netmagic-08-aug-2022-myapache:v1
 1288  docker images
 1289  docker ps
 1290  docker run -d  --name test-1 amitvashist7/devops-netmagic-08-aug-2022-myapache:v5
 1291  docker run -d  --name test-2 amitvashist7/devops-netmagic-08-aug-2022-myapache:v5
 1292  docker ps
 1293  curl 172.17.0.2
 1294  curl 172.17.0.3
```


```
 1307  docker ps
 1308  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -q)
 1309  curl 172.17.0.2
 1310  docker network ls
 1311  docker network inspect bridge
 1312  ip addr
 1313  curl 172.17.0.2
 1314  route -n
 1315  curl 172.17.0.2
 1316  docker ps
 1317  ip addr
 1318  docker run -d  --name test-3 -p 8081:80 amitvashist7/devops-netmagic-08-aug-2022-myapache:v1
 1319  docker ps
 1320  netstat -tulnp
 1321  docker inspect --format '{{.Name}} {{.State.Running}} {{.NetworkSettings.IPAddress}}' $(docker ps -q)
 1322  docker ps
 1323  systemctl status docker
 1324  docker ps
 1325  docker run -d  --name test-4 -p 8081:80 amitvashist7/devops-netmagic-08-aug-2022-myapache:v1
 1326  docker run -d  --name test-4 -p 8082:80 amitvashist7/devops-netmagic-08-aug-2022-myapache:v1
 1327  docker run -d  --name test-5 -p 8082:80 amitvashist7/devops-netmagic-08-aug-2022-myapache:v1
 1328  docker ps
 1329  docker images
 1330  docker inspect amitvashist7/devops-netmagic-08-aug-2022-myapache:v5
 1331  docker ps
 1332  history
 1333  docker run -d  --name test-6 -P  amitvashist7/devops-netmagic-08-aug-2022-myapache:v1
 1334  docker ps
 1335  docker run -d  --name test-7 -P  amitvashist7/devops-netmagic-08-aug-2022-myapache:v5
 1336  docker ps
 1337  docker run -d  --name test-8 -P  amitvashist7/devops-netmagic-08-aug-2022-myapache:v5
 1338  docker run -d  --name test-9 -P  amitvashist7/devops-netmagic-08-aug-2022-myapache:v5
 1339  docker ps
 1340  history
 1341  ls
 1342  cd 04-Docker/02-Docker-Images/apache/v4/
 1343  ls
 1344  cat Dockerfile
 1345  vim Dockerfile
 1346  docker build -t myapache:v6  .
 1347  ls
 1348  docker images
 1349  vim Dockerfile
 1350  docker build -t myapache:v6  .
 1351  docker images
 1352  docker run -d myapache:v6
 1353  docker ps
 1354  docker run -d -P myapache:v6
 1355  docker ps
 1356  docker run -d -p 9090:80 -p 9091:8080 -p 9092:3306 myapache:v6
 1357  docker ps
 1358  docker run -d -p 9095:80  myapache:v6
 1359  docker ps

```
