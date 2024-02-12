# PyStagram
instagram clone coding 으로 Hash Tag와 사진 공유, Follow 기능을 구현한 프로젝트 입니다.
DB는 python 제공 db인 SQLite를 이용하였습니다. DB 변경에 대한 설명은 [DB 변경](### DB 변경)

> PyStgram 사용법

0. git clone을 하신후 directory를 clone하여 만들어진 directory로 옮겨서

1. 의존성 모듈 설치를 완료합니다.
```
pip install -r requirements.txt
```


2. 모델들에 db migrate를 수행합니다. 순서는
  migration 을 만듭니다 -> 만든 migration으로 migrate를 동작하여 db에 적용해야합니다.
  사용 모듈은 django 자체 제공 manage.py 를 이용하면 됩니다.
```
python manage.py makemigrations 
python manage.py migrate
```

3. Makefile 을 이용해 make 동작으로 runserver를 합니다. Linux 환경에서 동작하는게 Make 프로그램이 기본적으로 깔려 있어 편합니다.

```
make
```

3-1. make 프로그램이 없다면 그냥 manage.py 의 runserver를 입력해주는 방식으로 서버 동작을 하면됩니다.
     runserver [host]:[port] 로 host와 port를 지정해줄수 있습니다. defualt는 host=localhost port=8000 입니다.
```
python manage.py runserver 0.0.0.0:8000
```

4. Browser를 통해 접속하여 사용하시면 됩니다.


### DB 변경
settings.py 를 변경해야하며
settings 안에 database 변수에 설정된 내용들을 변경하면됩니다. 
