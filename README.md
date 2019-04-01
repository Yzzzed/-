# 在线考试系统设计文档

## 目录

* [程序系统结构](#程序系统结构)

* [用户注册（user-zc）模块](#用户注册（user-zc）模块)

* [用户登录（login）模块](#用户登录（login）模块)

* [在线考试（onlineExam）模块](#在线考试（onlineExam）模块)

* [题库管理（question-gl）模块](#题库管理（question-gl）模块)

* [试卷管理（paper-gl）模块](#试卷管理（paper-gl）模块)

* [公告管理（notice-gl）模块](#公告管理（notice-gl）模块)

* [用户管理管理（user-gl）模块](#用户管理管理（user-gl）模块)

* [成绩查询（mark-cx）模块](#成绩查询（mark-cx）模块)

* [修改密码（pwd-xg）模块](#修改密码（pwd-xg）模块)

---

### 程序系统结构

```mermaid
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

---

### 用户注册（user-zc）模块

```mermaid
graph TD
    A[录入信息成功] --> B[接收信息]
    B --> C{输入的格式不正确?}
    C --no--> D{用户已存在吗?}
    D --no--> E[注册成功] 
    C --yes--> F[提示输入格式不正确]
    D --yes--> G[提示用户已存在]
    F --> A
    G --> A
```

---

### 用户登录（login）模块

```mermaid
graph TD
A[登录信息录入] --> B[接收登录信息]
B --> C{存在此用户名和密码组合?}
C --yes--> D[跳转到主页]
C --no--> E[提示用户名或密码不正确]
E --> A
```

---

### 在线考试（onlineExam）模块

```mermaid
    flowchat

    st=> start:开始
    en=> end:结束

    st->en

```
