# passport

## ����

1. npm init
2. express
3. router �� router ����
4. auth-router �� router �����
    - get : signin , signup
    - post : signin, signup, signout

5. sign.js ����
    - function - signIn(id,password) : �α��� �����ϸ� true, �����ϸ� false ��ȯ
    - function - signOut(id) : �α׾ƿ� �����ϸ� true, �����ϸ� false ��ȯ
    - function - signUp(id,password,name,email) : ȸ������ �����ϸ� true, �����ϸ� false ��ȯ

6. id,password �� post �� ���޹��� body ���� ���� body-parser 

6. passport.js ����
    - passport �� sign.js ������ �ʿ䰡 ����!
