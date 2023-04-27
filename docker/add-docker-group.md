# 특정 사용자 sudo 없이 docker 사용 설정

docker를 설치하면서 만들어진 docker 그룹에 사용자를 추가한다.

```bash
$ sudo usermod -aG docker [유저이름]
```

usermod -aG <그룹> <계정>
<계정>이 원래 그룹뿐 아니라 추가적(append)으로 <그룹>에도 포함되도록 하는 커맨드
