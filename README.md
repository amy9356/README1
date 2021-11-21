# sw_20185017


## 쉘스크립트 ***getopt*** 명령어
- 정의 : **실행옵션을 구현하는 명령어**
|분류|사용방법|
|---|---|
|인자가 있는 실행 옵션|옵션 뒤에 ":"를 입력|
|인자가 없는 실행 옵션|옵션만 정의|


- 예제
```while getopts "a:b:h" opt
do
case $opt in
a) arg_a=$OPTARG
echo "Arg A: $arg_a"
;;
b) arg_b=$OPTARG
echo "Arg B: $arg_b"
echo "$arg_b"
;;
h) help ;;
?) help ;;
esac
done
```

***
## 쉘스크립트 ***getopts*** 명령어
- 정의 : 
- 사용 방법 : 
- 예제 : 
- 주의 할 점 : 


***
## 리눅스 ***sed*** 명령어
- 정의 : 
- 사용 방법 : 
- 예제 : 
- 주의 할 점 : 


***
## 리눅스 ***awk*** 명령어
- 정의 : 
- 사용 방법 : 
- 예제 : 
- 주의 할 점 : 
