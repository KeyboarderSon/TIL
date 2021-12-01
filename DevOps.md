## ngrok
외부(public)에서 localhost에 접속할 수 있게 도와주는 터널링 프로그램  
ex) 나의 로컬 pc가 웹 서버 역할을 할 때  
세션이 만료되면 재실행해야 한다.  
```ngrok http 8000```

```
ngrok by @inconshreveable                                                                                             (Ctrl+C to quit)

Session Status                online
Version                       2.3.40
Region                        United States (us)
Web Interface                 http://127.0.0.1:4040
Forwarding                    http:/1234-567-891-234-56.ngrok.io -> http://localhost:8000
Forwarding                    https://1234-567-891-234-56.ngrok.io -> http://localhost:8000

Connections                   ttl     opn     rt1     rt5     p50     p90
                              3       0       0.00    0.00    5.20    5.22
```

