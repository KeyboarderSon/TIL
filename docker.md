## Docker Container 만들기
```docker run --runtime=nvidia -itd --name <container nickname> -v <mapping 하고싶은 dir>:<mapping 당하는 dir> <docker image> bash```

* ```--runtime=nvidia``` 혹은 ```--gpus all``` 사용하면 된다.
* ```-v dir:dir``` : 컨테이너에서 내 로컬 경로를 지정해주고 그 로컬 경로 활용하여 작업이 가능하다.

## Docker run 상태로 빠져나오기
```ctrl + p,q```

## 이어서 진행하기
```docker attach <container nickname>```