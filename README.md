# MyBatisSetting

### OracleDB에서 기본으로 제공하는 SCOTT 데이터베이스 기반으로 세팅해놨습니다
### ID : SCOTT
### ID : TIGER

아래와 같이 SQL Devloper에서 미리 세팅해놔야 합니다
``` sql
-- users테이블 생성
create table users(
    id number primary key,
    username varchar2(20),
    password varchar2(20),
    email varchar2(50),
    createdAt TIMESTAMP
);

CREATE SEQUENCE users_seq 
INCREMENT BY 1 
START WITH 1;

-- 더미데이터 추가
insert into users(id, username, password, email, createdAt) values(users_seq.nextval, 'ssar', '1234', 'ssar@nate.com', sysdate);
insert into users(id, username, password, email, createdAt) values(users_seq.nextval, 'cos', '1234', 'cos@nate.com', sysdate);
insert into users(id, username, password, email, createdAt) values(users_seq.nextval, 'hong', '1234', 'hong@nate.com', sysdate);
commit;
```
