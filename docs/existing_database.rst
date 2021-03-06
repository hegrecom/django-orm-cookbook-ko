이미 존재하는 데이터베이스를 어떻게 장고 모델로 변환하는가?
=====================================================

| Django 에는 존재하는 데이터베이스를 검토하여 모델로 생성할 수 있는 ``inspectdb`` 라는 기능이 있습니다.
| 다음과 같은 명령어로 결과를 확인할 수 있습니다.


::

    $ python manage.py inspectdb

| 실행하기 전 반드시 ``settings.py`` 파일에 변환하려는 데이터베이스를 정의해야 합니다.
| 결과는 각 테이블의 모델을 담은 파일이 될 것입니다.

다음과 같이 파일을 저장할 수 있습니다.

::

    $ python manage.py inspectdb > models.py

위의 명령으로 결과 파일이 현재 디렉토리에 저장될 것입니다. 해당 파일을 앱의 올바른 위치로 이동시키면 추가적인 커스텀을 시작할 수 있게 됩니다.
