```
 2019  mkdir 01-Inventory
 2020  ls
 2021  cd 01-Inventory/
 2022  ls
 2023  vim hosts
 2024  ls
 2025  ansible all -i hosts -m ping -u vagrant -k
 2026  apt-get install sshpass -y
 2027  ansible all -i hosts -m ping -u vagrant -k
 2028  ssh vagrant@172.31.0.100
 2029  ansible all -i hosts -m ping -u vagrant -k
 2030  ssh vagrant@172.31.0.101
 2031  ssh vagrant@172.31.0.102
 2032  ls
 2033  cat /root/.ssh/known_hosts
 2034  ansible all -i hosts -m ping -u vagrant -k
```


```
 2060  ansible web -i hosts -m ping -u vagrant -k
 2061  ansible db -i hosts -m ping -u vagrant -k
 2062  ansible ansible -i hosts -m ping -u vagrant -k
 2063  ls
 2064  vim hosts
 2065  ls
 2066  ansible web -i hosts -m ping -u vagrant -k
 2067  ansible db -i hosts -m ping -u vagrant -k
 2068  ansible prod -i hosts -m ping -u vagrant -k
 2069  ansible stage -i hosts -m ping -u vagrant -k
 2070  cat hosts
 2071  ansible 'prod:&web' -i hosts -m ping -u vagrant -k
 2072  ansible 'stage:&web' -i hosts -m ping -u vagrant -k
 2073  ansible 'stage:&db' -i hosts -m ping -u vagrant -k
 2074  cat hosts
 2075  vim hosts
 2076  ansible 'prod:&web' -i hosts -m ping -u vagrant -k
 2077  ansible 'prod:&web:!ansible' -i hosts -m ping -u vagrant -k
 2078  ls
 2079  vim hosts
 2080  vi hosts
 2081  ls
 2082  ansible 'dc' -i hosts -m ping -u vagrant -k
 2083  ansible 'all' -i hosts -m ping -u vagrant -k
 2084  ls
 2085  cat hosts
 2086  vim hosts
 2087  ls
 2088  ansible 'dc' -i hosts -m ping
 2089  ansible 'web' -i hosts -m ping
 2090  ansible 'db' -i hosts -m ping
```
