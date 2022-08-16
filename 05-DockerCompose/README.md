```
 2012  mkdir 05-DockerCompose/00-Setup -p
 2013  cd 05-DockerCompose/00-Setup/
 2014  ks
 2015  ls
 2016  vim dockercompose-install.sh
 2017  ls
 2018  chmod +x dockercompose-install.sh
 2019  ls
 2020  ./dockercompose-install.sh
 2021  ls
 2022  docker-compose version
 2023  ls
 2024  cd ..
 2025  ls
 2026  mkdir 01-Nginx
 2027  ls
 2028  cd 01-Nginx/
 2029  ls
 2030  vim docker-compose.yaml
 2031  ls
 2032  docker-compose up
 2033  docker-compose up -d
 2034  docker-compose ps
 2035  docker ps
 2036  ip addr
 2037  ls
 2038  cd ..
 2039  ls
 2040  cp -rf 01-Nginx 02-Multi-App
 2041  ls
 2042  docker images
 2043  ls
 2044  vim 02-Multi-App/
 2045  vim 02-Multi-App/docker-compose.yaml
 2046  ls
 2047  cd 02-Multi-App/
 2048  ls
 2049  docker-compose ps
 2050  cd ..
 2051  cd 01-Nginx/
 2052  ls
 2053  docker-compose ps
 2054  docker-compose stop
 2055  docker-compose ps
 2056  docker-compose rm
 2057  docker-compose ps
 2058  docker ps -a
 2059  docker rm $(docker ps -qa)
 2060  docker ps -a
 2061  ls
 2062  cd ..
 2063  ls
 2064  cd 02-Multi-App/
 2065  ls
 2066  docker-compose ps
 2067  docker-compose up -d
 2068  docker-compose ps
 2069  docker-compose stop
 2070  docker-compose rm
 2071  docker images
 2072  vim docker-compose.yaml
 2073  docker-compose up -d
 2074  docker-compose ps
 2075  docker ps
 2076  ls
 2077  vim docker-compose.yaml
 2078  docker-compose up -d
 2079  docker-compose ps
 2080  docker-compose up -d
 2081  vim docker-compose.yaml
 2082  docker-compose up -d
 2083  docker-compose ps
 2084  vim docker-compose.yaml
 2085  ls
 2086  docker-compose ps
 2087  docker ps
 2088  cat docker-compose.yaml
 2089  docker-compose up -d
 2090  docker-compose stop
 2091  ls
 2092  cd ..
 2093  ls
 2094  history
 2095  cat 02-Multi-App/docker-compose.yaml
```


```
 2131  mkdir 04-Petclinic-Deploy
 2132  ls
 2133  cd 04-Petclinic-Deploy/
 2134  ls
 2135  cat ../03-Stack/docker-compose.yaml
 2136  ls
 2137  cp -rf ../03-Stack/docker-compose.yaml .
 2138  ls
 2139  vim docker-compose.yaml
 2140  ls
 2141  vim Dockerfile
 2142  ls
 2143  cp -rf /root/petclinic.war .
 2144  ls
 2145  docker-compose up -d
 2146  docker-compose ps
 2147  ls
 2148  docker-compose up -d
 2149  docker-compose up -d --build
 2150  vim Dockerfile
 2151  docker-compose up -d
 2152  docker-compose up -d --build
 2153  ls
 2154  > petclinic.war
```
