# ������ Node.js + MySQL ȸ�� ����, �α��� �����

## ��ǥ

* �����ϰ� �α��� ȸ������ ��� �Ǵ� web application

## TODO

1. DB
    1. DB ����
        * User Table ���� : ID, Password, email, name
    2. DB �����

2. Front
    * Sign In Page
        * Input : ID , Password
        * Button : Sign In , Sign Up
    * Sign Up Page
        * Input : ID , Password , email , name
        * Button : Sign Up

3. Back
    1. Connect DB
    2. app.get
        * Sign In page
        * Sign Up page
    3. app.post
        * Sign In : ID, Password
        * Sign Up : ID , Password, email, name ���� Create

## �߰� �ؾ��� ��

* app.js �� �ִ� db ���� �����
* password ��ȣȭ
* id or email �ߺ� �˻� ���
* ���� �� ���� ���
* email, password �� ���� �˻� ���

* authentication ���
* ID/Password ã�� ���
* cookie �̿��� login ���� ������Ű��

## ����� sql ��

1. DataBase �����
    ```
        create database study_db;
    ```

2. Table �����
    ```
        create table users(
            _id int primary key auto_increment,
            id varchar(32) not null,
            password varchar(32) not null,
            name varchar(32) not null,
            email varchar(64) not null
        )
    ```
3. Insert
    ```
        // command line ���� ���
        insert into users (id,password,name,email) valuew ('a','b','c','d')
    ```
    ```
        // app.js ���� ���
        insert into user SET ?
    ```
4. Select
    ```
        // command line ���� ���
        select * from users
        select * from users where id = 'a'
        select id from users where id = 'a'
    ```
    ```
        // app.js ���� ���
        select * from user where id = ?
    ```