# SSL Verifizerung abschalten, umgehen 

```
# Wenn eine Fehler auftritt, wie z.B. beim Pushen 
fatal: unable to access 'https://bitbucket.org/xy/xyz.git/': SSL certificate problem: unable to get local issuer certificate

git config http.sslVerify false

oder: für alle repos
git config --global http.sslVerify false
```
