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

7. passport.js ����
    - passport �� sign.js ������ �ʿ䰡 ������.
    - �α���, �α׾ƿ� ó���� ���ش�.
    - sign.js �� ȸ�����Ը� �ֱ⿡�� ������ ����. auth.js ���� ó������.

8. sign.js ����

9. passport.js ����
    1. passport.js �� app ��ü�� �ʿ��ϰ� auth.js �� passport ��ü�� �ʿ��ϴ�.
        - ���1 - ��Ȱ�ڵ�
            1. app.js ���� passport �� app �� �����ؼ� 
            2. app ���� passport ����� ( require(passport)(app) )
            3. auth.js �� �����ϱ� ( require(auth)(passport) )
        - ���2 - �� ����
            1. app.js ���� auth �� app �� �����ϰ� ( require(auth)(app) )
            2. auth ���� passport �� app �� �����ؼ� passport �� �����. ( require(passport)(app) )
        - ���1 ����. passport �� ���̺귯���� app ���� ����ϴ°� �� ������� �� ����.
        - �� app �� passport �� ����ߴ�. �׸��� passport �� app ���ݿ��� �α��� ���¸� Ȯ���ϱ� ������ �̰� �� ���� ������ ����.
        - �ϴµ� module �� �Ű����� �� �� �������� return router; or return passport; ���ؼ� �� �Ծ���.
    2. npm install passport module
        - package �̸��� passport �� install �� �ȵƾ���.
        - npm install �� �� -s �� ���ϴϱ� �αװ� ����
    3. npm install passport strategy
    4. passport �� session �� �ʿ�
        - npm install express-session
        - express-session require
        - �ɼ� ����
        - session ���� �� �� ���� (file ���� ����)  
    5. passport ���� ����, post ���� �� � �� �о� ����, �о ��� �Ǵ����� ����
        - app.use(new LocalStrategy()) �κ�
        - db library ���� db.selectUser , db.insertUser �� �Լ��� ��������� �񵿱������� db �� ó���Ǽ� db sql ����� ������ ���� value �� return �ż� value �� undefiend �ƴ�.
        - �񵿱� ó�� ���� ���ΰ� �� �ʿ��ϴٰ� ������ ���.
        - �׷��� �ϴ��� db library �ۼ��ߴ� ���� �����.
    7. session ó��
        - serializeUser, deserializeUser �κ�