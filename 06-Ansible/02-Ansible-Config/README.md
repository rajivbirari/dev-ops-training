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

```
1981  cp -rf 01-Inventory 02-Ansible-Config
 1982  ls
 1983  cd 02-Ansible-Config/
 1984  s
 1985  ;s
 1986  ls
 1987  vim hosts
 1988  ls
 1989  ansible 'web' -i hosts -m ping
 1990  vim ansible.cfg
 1991  ls
 1992  vim /etc/ansible/ansible.cfg
 1993  ls
 1994  vim ansible.cfg
 1995  ls
 1996  cat ansible.cfg
 1997  ansible 'web' -i hosts -m ping
 1998  ansible 'web'  -m ping
 1999  > /root/.ssh/known_hosts
 2000  exit
 2001  ls
 2002  cd devops-netmagic-08-Aug-2022/
 2003  ls
 2004  cd 06-Ansible/02-Ansible-Config/
 2005  ls
 2006  ansible 'web'  -m apt -a "name=tree state=present" -s
 2007  ansible 'web'  -m apt -a "name=tree state=present"
 2008  ansible 'web'  -m apt -a "name=ntp state=present"
 2009  ls
 2010  grep -A5 "privilege" /etc/ansible/ansible.cfg
 2011  grep -A5 "privilege" /etc/ansible/ansible.cfg  >> ansible.cfg
 2012  vim ansible.cfg
 2013  ansible 'web'  -m apt -a "name=ntp state=present"
 2014  ls
 2015  grep -i "log_path"  /etc/ansible/ansible.cfg
 2016  grep -i "log_path"  /etc/ansible/ansible.cfg   >> ansible.cfg
 2017  vim ansible.cfg
 2018  ls
 2019  ls -ltr /var/log/ans*
 2020  ansible 'web'  -m apt -a "name=ntp state=present"
 2021  ansible 'web'  -m apt -a "name=ntp state=absent"
 2022  ls -ltr /var/log/ans*
 2023  tail -f /var/log/ansible.log
 2024  less  /var/log/ansible.log
 2025  ls
 2026  cat /etc/os-release
 2027  ansible 'web'  -m command -a "cat /etc/os-release"
 2028  cat /etc/*-relase
 2029  cat /etc/*-release
 2030  ansible 'web'  -m command -a "cat /etc/os-release"
 2031  ansible 'web'  -m command -a "cat /etc/*-release"
 2032  cat /etc/*-release
 2033  ansible 'web'  -m command -a "uname -a "
 2034  ansible 'web'  -m command -a "ip addr"
 2035  ansible 'web'  -m command -a "cat /etc/*-release"
 2036  ansible 'web'  -m shell -a "cat /etc/*-release"

```
