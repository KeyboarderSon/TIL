## ssh로 server에 붙기
```ssh -l 계정명 -p port_num server주소```

## 파일 server에 업로드
### 구글 드라이브 링크로 파일 받기
* 링크를 모든 사용자에게 공개한 상태로 공유하게 되면 링크의 생긴 형태는 다음과 같다.
* **ID** 부분을 넣어주면 된다. 
   
https://drive.google.com/file/d/**ID**/view...  
~~~
curl -c ./cookie -s -L "https://drive.google.com/uc?export=download&id=<ID>" > /dev/null  
curl -Lb ./cookie "https://drive.google.com/uc?export=download&confirm=`awk '/download/ {print $NF}' ./cookie`&id=<ID>" -o FILENAME
~~~

* 여러개의 큰 용량이더라도 zip파일로 묶어서 한번에 upload할 수 있다.

### wget으로 tar파일 가져오기
* tar 파일 받고 압축 해제
```
wget -c https:~.tar.gz -O - | tar -xz
```