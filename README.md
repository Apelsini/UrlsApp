# UrlsApp
 URL links shortener diplom app

# ���������:
- ��������� �� ������� u9.by
- �� �������� DatetimePicker � ������ Customer - JavaScript
- ������ �� ������������� �� ������ ����� ���� ��: � �� ���� �����:
# ����� �� �������
- �������� ������ ��������� ������� �� ��������� ������
- �������� ������������� ������ �� ��������� ����������
- ���������� ����������� �� ������� ��� � �������� Customer

��� ������� ������� �� ���������� ����� 

```shell
docker compose up
docker compose -f docker-compose-deploy.yml up --build
```
����� �������� ������� ����� ����� �� ����� ���������:

```shell
docker compose exec app python manage.py migrate
```

��� ������� ����� ���������� ����� ������: `relation "django_session" does not exist`
��� ������ ��� ���� ���� �� ������ ��������. � ����� ���� ��������� ��������� ������� ��� � �����: `docker compose exec app python manage.py migrate`
������ ��� ������� �������� � ������ �� ������� �� �� � ������ �� ����������.

����� ��������� ������ ��������:

```shell
docker compose down
```