# 接口：studentChoose
用例：[选课](../用例/用例_选课.md)
* 功能：学生对老师创建的课程进行选择
* 权限： 学生：选择课程
* API请求地址： 接口基本地址/v1/api/studentChoose
* 请求方式 ：POST
* 请求实例：
    {
        "student_id":201510414320,
        "teacher_students_class":001
    }
* 请求参数说明:

|参数名称|说明|
|:---:|:---:|
|student_id|学号|
|teacher_students_class|选择的老师班级|

* 返回实例：
    {
        "status": true,
        "info": null
    }
* 返回参数说明：

|参数名称|说明|
|:---:|:---:|
|status|bool类型，true表示正确的返回，false表示有错误|
|info|返回结果说明信息|