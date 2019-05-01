# Improve Project2 - SignUp and SignIn

## TODO

1. Hide db description 
2. Encrypt the password
3. Check the overlap of ID or email
4. Limit the number of character
5. Check the format of password or email
6. Make authentication
7. Make function finding ID or password
8. Maintain the signin state by using session and make logout

### Hide db description

1. db data �� �ٸ� ���Ͽ� ���ȭ ��Ų �� gitignore �� �� dbdata �� �ø��� �ʴ´�.
    * gitignore �� �����ߴµ� ��ȭ�� ������ 
    * git rm -r --cached . �� ĳ��??�� ����� �ٽ� �ߴ��� �ƴ�.
    * �̹� �ö� �ִ� log �� ���� ������� �ߴ�.

### Encrypt the password

* PBKDF2(Password-Based Key Derivation Function2)
    1. npm ���� ��� ��ġ
    2. table �� salt �÷� �߰�
    3. database �� password �÷� ���� ���� (varchar(10)->varchar(200))
    2. ȸ������ �� ��й�ȣ ��ȣȭ �Ǿ� ����ǰ�
    3. �α��� �� �Է��� ��й�ȣ ��ȣȭ ���Ѽ� db�� ����� ��ȣȭ �� password �� ��