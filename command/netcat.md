
## send hex http header
```bash
echo -e '\x80' | nc host port
echo -en 'GET / HTTP/1.1\r\nHost: example.com\r\nFunny: ho\0ho\nho\r\n\r\n' | nc IP PORT
echo -en 'GET / HTTP/1.1\r\nHost: \xfffe.com\r\nFunny: ho\0ho\nho\r\n\r\n' | nc IP PORT
```

## 快速端口存活检测
### 立即返回
```bash 
nc -n -z -w $TIMEOUT $IP $PORT 2>&1
```
### timeout时间后才返回
```bash 
nc -n -w $TIMEOUT $IP $PORT 2>&1
```