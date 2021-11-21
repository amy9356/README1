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
- 정의 : **옵션을 파싱하는 명령어**
- 예제 
```
while getopts "ap:" option  
    do
        case $option in
            a)
                a_flag = 1
                ;;
            p)
                separator="$OPTARG"
                ;;
            \?)
                echo "Usage: getopts.sh [-a] [-p separator] target_dir" 1>&2 # 해당 Usage 를 error 스트림으로 출력한다.
                exit 1
                ;;
        esac
    done
```

***
## 리눅스 ***sed*** 명령어
- 정의 : 
- 사용 방법 : 
- 예제 : 



***
## 리눅스 ***awk*** 명령어
- 정의 : **텍스트 형태로 되어있는 입력 데이터를 행과 단어 별로 처리해 출력**
- 기능 : ***지정된 파일로부터 데이터를 분류, 분류된 텍스트 데이터를 바탕으로 패턴 매칭 여부를 검사하거나 데이터 조작 및 연산 등의 액션을 수행, 그 결과를 출력하는 기능을 수행***
- 사용 방법 : pattern { action }
- 예제 

|사용 예|명령어옵션|
|---|---|
|파일전체내용출력|```awk '{ print }' [FILE]```|
|필드값 출력|```awk '{ print $1 }' [FILE]```|
|필드 값에 임의 문자열을 같이 출력|```awk '{print "STR"$1, "STR"$2}' [FILE]```|
|지정된 문자열을 포함하는 레코드만 출력|```awk '/STR/' [FILE]```|
|특정 필드 값 비교를 통해 선택된 레코드만 출력|```awk '$1 == 10 { print $2 }' [FILE]```|
|특정 필드들의 합 구하기|```awk '{sum += $3} END { print sum }' [FILE]```|
|여러 필드들의 합 구하기|```awk '{ for (i=2; i<=NF; i++) total += $i }; END { print "TOTAL : "total }' [FILE]```|
|레코드 단위로 필드 합 및 평균 값 구하기|```awk '{ sum = 0 } {sum += ($3+$4+$5) } { print $0, sum, sum/3 }' [FILE]```|
|필드에 연산을 수행한 결과 출력하기|```awk '{print $1, $2, $3+2, $4, $5}' [FILE]```|
|레코드 또는 필드의 문자열 길이 검사|```awk ' length($0) > 20' [FILE]```|
|레코드 또는 필드의 문자열 길이 검사|```awk -f [AWK FILE] [FILE]```|
|파일에 저장된 awk program 실행|```awk -f [AWK FILE] [FILE]```|
|필드 구분 문자 변경하기|```awk -F ':' '{ print $1 }' [FILE]```|
|awk 실행 결과 레코드 정렬하기|```awk '{ print $0 }' [FILE]```|
|특정 레코드만 출력하기|```awk 'NR == 2 { print $0; exit }' [FILE]```|
|출력 필드 너비 지정하기|```awk '{ printf "%-3s %-8s %-4s %-4s %-4s\n", $1, $2, $3, $4, $5}' [FILE]```|
|필드 중 최대 값 출력|```awk '{max = 0; for (i=3; i<NF; i++) max = ($i > max) ? $i : max ; print max}' [FILE]```|
