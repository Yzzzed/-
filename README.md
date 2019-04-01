 在线考试系统设计文档

=====================

目录

-----

* [程序系统结构](#程序系统结构)

* [用户注册（user-zc）模块](#用户注册（user-zc）模块)

*  [用户登录（login）模块](#用户登录（login）模块)

* [在线考试（onlineExam）模块](#在线考试（onlineExam）模块)

*  [题库管理（question-gl）模块](#题库管理（question-gl）模块)

*  [试卷管理（paper-gl）模块](#试卷管理（paper-gl）模块)

* [公告管理（notice-gl）模块](#公告管理（notice-gl）模块)

* [用户管理管理（user-gl）模块](#用户管理管理（user-gl）模块)

* [成绩查询（mark-cx）模块](#成绩查询（mark-cx）模块)

* [修改密码（pwd-xg）模块](#修改密码（pwd-xg）模块)

---------

### 程序系统结构

``` mermaid
    graph LR
    A[在线考试系统] --- B[管理员功能]
    A --- C[用户功能]
    A --- D[用户注册]
    A --- E[用户与管理员登录]
    B --- F[用户管理]
    B --- G[试卷管理]
    B --- H[题库管理]
    B --- I[成绩查询]
    B --- J[公告管理]
    C --- K[修改密码]
    C --- L[在线考试]
    C --- M[查询成绩] 
```

### 用户注册（user-zc）模块

``` flow
    in=>operation:录入用户信息
    reSuccess=>operation:注册成功
    acc=>operation:接收信息
    formatFalse=>operation:提示输入格式不正确
    userExist=>operation:提示用户已存在
    inFalse=>condition:输入的格式不正确？
    isExist=>condition:用户已存在吗？

    in->acc->inFalse
    inFalse(yes)->formatFalse
    inFalse(no)->isExist
    isExist(yes)->userExist
    isExist(no)->reSuccess
```
