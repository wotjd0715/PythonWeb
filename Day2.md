# Chapter2 장고 시작하기
## 2.1 파이썬과 파이참 설치하기
- [파이썬 설치하러가기](www.python.org)
- [파이참 설치하러가기](wwww.jetbrains.com/pycharm/download/)

## 2.2 프로젝트 생성하기
1. Pycharm창에서 Create New Project 누르기

2. `Loction:/User/~~~~/untitled`에서 `untitled`부분에 자신이 원하는 project명 넣기

3. create 버튼 누르기!   
![git](https://github.com/wotjd0715/PythonWeb/blob/master/images/d2p1.png)   
4. 사진의 1번에 자신이 만든 project안에 `venv`라는 가상 환경 폴더가 생성된 것을 확인 하고
 2번 terminal을 눌른다.   
  
5. 이제 장고를 설치해 줍니다.
   ```python
   pip install django  
    ```
   장고 설치가 완료되면 장고 프로젝트를 만듭니다.
   ```python
   django-admin startproject config .
   ```
   ![git](https://github.com/wotjd0715/PythonWeb/blob/master/images/d2p2.png)   
    
   성공적으로 프로젝트를 만들었다면 cofig폴더와 manage.py가 생성됩니다.
   
6. 마지막으로 데이터베이스를 초기화 하면서 생성해 줍니다.
   ```python
   python manage.py migrate
   ```
   ![git](https://github.com/wotjd0715/PythonWeb/blob/master/images/d2p3.png)   
   프로젝트 창에 새롭게 db.sqlite3이 만들어 진것을 확인할수 있습니다.
   이 파일애 우리가 웹 프로그래밍에서 다루는 회원 정보, 글 정보가 저장됩니다.
   
 ## 2.3 프로젝트 구조 살펴 보기
 >config
>>init.py: 파이썬 2.x대 버전과 호환, 비어있음   
>>settings.py: 프로젝트에 관련된 다양한 설정   
>>urls.py: url을 설정 해주는 것   
>>wsgi.py:웹 서비스를 실행하기 위한 wsgi 

>venv: 프로젝트 구동애 필요한 가상환경이 들어있는 폴더입니다.

>db.sqlite3: SQLite3 DB파일 입니다.

>manage.py: 장고의 다양한 명령어를 실행하기 위한 파일입니다.

## 2.4 장고 기본 명령들

<https://gigas-blog.tistory.com/m/98?category=861837>

## 2.5 디자인 패턴이란?
디자인 패턴이란? **설계를 효율적으로 하기위한 구조**   

#### 종류    
>**DB구조 결정 - 사용자에게 보여지는 UI - 기능&로직 부분**  
>- MVX(Model-View-Controller)
>- MTV(Model-Template-View) -> Django   

이제 앱을 생성하기 위해 다음 명령어를 입력합니다.
```python
python manage.py startapp app_default
```

## 2.6 관리자 계정 생성하기

```python
python manage.py createsuperuser
```
코드 입력후 차례대로 입력하면 관리자 계정이 생성됩니다.   
```
Username:    
Email address:    
Password: (원래 입력해도 표시되지 않습니다.)
Password (again): (원래 입력해도 표시되지 않습니다.)
```

## 2.7 사이트 확인하기
이제 서버를 실행해 봅니다
```python
python manage.py reunserver
```
terminal에 뜨는 `http://127.0.0.1:8000/`를 클릭해 자신의 웹 사이트에 들어 가봅니다.   
![git](https://github.com/wotjd0715/PythonWeb/blob/master/images/d2p4.png)   
추가로 웹 브라우저에 `http://127.0.0.1:8000/admin`을 입력할경우 관리자 화면으로 접속 가능 합니다.   
![git](https://github.com/wotjd0715/PythonWeb/blob/master/images/d2p5.png)
