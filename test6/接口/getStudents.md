# 接口：getStudents
用例：[学生列表](../用例/用例_学生列表.md)
* 权限：学生/访客：不能看到RESULT_SUM，WEB_SUM    老师：可以看到RESULT_SUM，WEB_SUM。
* 功能：返回所有学生的列表。
* API请求地址： 接口基本地址/v1/api/getStudents/<semester_id>/<course_id>/<class_id>
* 请求方式 ：GET
* 请求参数说明: 

|参数名称|说明|
|:---:|:---:|
|semester_id|选择的学期编号|
|course_id|选择的课程编号|
|class_id|选择的班级号|

* 返回实例：
    {
          "status": true,
          "info": null,
          "total": 121,
          "semester_id":20151
          "course_id":001
          "class_id":3
          "data": [
              {"WEB_SUM": "Y,Y,Y,Y,Y,N",
              "RESULT_SUM": "83.75,90,80,80,85,N",
              "GITHUB_USERNAME": "xiechao.neddy@foxmail.com",
              "STUDENT_ID": "201510414320",
              "CLASS": "软件(本)15-3",
              "NAME": "谢超",
              "UPDATE_DATE": "2018-05-31 13:48:01"},
              {
              ...其他学生
              }
          ]
    }
* 返回参数说明：

|参数名称|说明|
|:---:|:---:|
|status|bool类型，true表示正确的返回，false表示有错误|
|info|返回结果说明信息|
|total|返回学生人数|
|semester_id|返回学期号|
|course_id|返回课程号|
|class_id|返回班级号|
|data|所有学生的数组|
|WEB_SUM|网址是否正确的汇总|
|RESULT_SUM|成绩的汇总|
|GITHUB_USERNAME|GITHUB 用户名|
|STUDENT_ID|学号|
|CLASS|班级|
|NAME|真实姓名|
|UPDATE_DATE|GitHUB用户名修改日期|