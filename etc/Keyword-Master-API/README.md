# 특징
> 키워드마스터에서 다운받은 csv파일을 폴더별 각각 상위 5개의 키워드를 추출하고, 그 결과를 json 형태로 반환하는 Flask API를 생성합니다.




# 사용 방법:

> [키워드마스터](https://whereispost.com/keyword/)에서 csv파일을 다운받습니다.
![image](https://user-images.githubusercontent.com/108644811/226158616-840e2938-f77f-4418-a26c-f08e955bcb1e.png)

> 다운받은 파일을 상위폴더 내의 하위폴더들에 각각 분류합니다.
![image](https://user-images.githubusercontent.com/108644811/226158659-6d2b04b6-2089-4289-8894-1d0fe877ece7.png)

> 폴더 경로, 파일 확장자, 하위 폴더 이름 리스트를 입력하여 Ranker 객체를 생성합니다.
![image](https://user-images.githubusercontent.com/108644811/226158627-6ac3a8ce-9b20-4593-8c74-d1d641cbdedc.png)


main.py 파일을 실행합니다.

생성한 Ranker 객체의 run 메소드를 실행합니다.

http://localhost:5000/home 에 접속하여 결과를 확인합니다.


# 실행결과:
![image](https://user-images.githubusercontent.com/108644811/226158452-c11c9daa-cfdb-41a8-a4d4-6a9b484f1c53.png)


# 참고 사항:

csv 파일 내부의 "총조회수" 컬럼은 쉼표(,)가 포함된 문자열로 되어 있기 때문에, 이를 숫자형으로 변환한 뒤 정렬합니다.
추출된 키워드는 열 이름을 리스트 형태로 넣어야 합니다.

JSON 파일을 한글로 출력하려면 app.config['JSON_AS_ASCII'] = False 옵션을 추가해야 합니다.
