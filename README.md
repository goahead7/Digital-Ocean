
```
root@ubuntu-s-1vcpu-1gb-nyc3-01:~# ping 185.57.28.200
PING 185.57.28.200 (185.57.28.200) 56(84) bytes of data.
^C
--- 185.57.28.200 ping statistics ---
7 packets transmitted, 0 received, 100% packet loss, time 6135ms
```

```
MacBook-Pro-Sofa:~ sophiakuznetsova$ ping 138.197.2.147
PING 138.197.2.147 (138.197.2.147): 56 data bytes
64 bytes from 138.197.2.147: icmp_seq=0 ttl=47 time=250.449 ms
64 bytes from 138.197.2.147: icmp_seq=1 ttl=47 time=246.656 ms
64 bytes from 138.197.2.147: icmp_seq=2 ttl=47 time=247.423 ms
64 bytes from 138.197.2.147: icmp_seq=3 ttl=47 time=247.542 ms
64 bytes from 138.197.2.147: icmp_seq=4 ttl=47 time=707.792 ms
^C
--- 138.197.2.147 ping statistics ---
6 packets transmitted, 5 packets received, 16.7% packet loss
round-trip min/avg/max/stddev = 246.656/339.972/707.792/183.914 ms
```

```
root@ubuntu-s-1vcpu-1gb-nyc3-01:~# ping google.com
PING google.com (172.217.12.206) 56(84) bytes of data.
64 bytes from lga25s63-in-f14.1e100.net (172.217.12.206): icmp_seq=1 ttl=118 time=2.19 ms
64 bytes from lga25s63-in-f14.1e100.net (172.217.12.206): icmp_seq=2 ttl=118 time=1.62 ms
64 bytes from lga25s63-in-f14.1e100.net (172.217.12.206): icmp_seq=3 ttl=118 time=1.59 ms
64 bytes from lga25s63-in-f14.1e100.net (172.217.12.206): icmp_seq=4 ttl=118 time=1.61 ms
64 bytes from lga25s63-in-f14.1e100.net (172.217.12.206): icmp_seq=5 ttl=118 time=1.60 ms
^C
--- google.com ping statistics ---
5 packets transmitted, 5 received, 0% packet los
```

Headers of Request/Response

1. vk.сom. Заметила очень много куки, но это было ожидаемо, а вот использование server: kittenx удивило, так как такого раньше не видела

2. GitHub.Com. Вроде ничего необычного, много куки, так же как и у вк, но вот у вк cache-control: no-store а у git cache-control: no-cache, попытаюсь разобраться в чем разница

3. https://univer.dvfu.ru/ мой универ. Обратила внимание вот на что: Expires: Thu, 19 Nov 1981 08:52:00 GMT, почему такая дата?

4. https://ru.wikipedia.org На первый взгляд ничего необычного.

На самом деле, пока особо не разобралась: что? зачем? почему? достаточно сложно анализировать. Поэтому будет круто проделать тоже самое и посмотреть на результат, когда количество знаний по теме будет больше.

2 Social Authentication

1.  mail.ru 
Первыми отправляются пакетные файлы, затем при авторизации отправляется домен, логин и username и 2 пароля 

2.vk.com 
Как я поняла, при запросе отправляет незашифрованный логин и пароль
