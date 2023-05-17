# 유저 생성

```bash
db.createUser({
"user" : "[유저이름]",
"pwd" : "[비밀번호]",
roles: [ "dbAdmin", "readWrite"]
});
```