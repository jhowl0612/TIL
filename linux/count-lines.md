# 파일 행 수 세기


`wc` = `word count`를 의미함.
```bash
$  wc fileName.txt
[행 수]  [단어 수]  [문자 수]  fileName.txt  
```

`-l` / `-w` / `-c` 옵션 사용 시 각각 행 / 단어 / 문자 수만을 출력하도록 한다

파이프라인을 사용하여, 타 커맨드의 출력에 대하여 사용 가능
```bash
$  find [디렉토리경로] -type f -name "[파일명*]" | wc -l
```
