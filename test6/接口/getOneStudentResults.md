# 接口：getOneStudentResults
用例：[查看成绩](../用例/用例_查看成绩.md)，[评定成绩](../用例/用例_评定成绩.md)
* 功能：返回一个学生的所有实验成绩和实验评价。
* 权限： 学生：只能查看自己的成绩，即接口参数student_id必须等于登录学生的student_id 老师：可以查看所有学生的成绩。
* API请求地址： 接口基本地址/v1/api/getOneStudentResults/<student_id>
* 请求方式 ： GET
* 请求参数说明:

|参数名称|说明|
|:---:|:---:|
|student_id|学生的学号|
* 返回实例：
    {         
          "status": true,
          "info": null,    
          "student_id": "201510414320", 
          "github_username": "neddy1995", 
          "class": "软件(本)15-3", 
          "name": "谢超", 
          "total": 6,
          "avgresult":90.5,       
          "data": [
              {
              "test_id":1,
              "web_exists": true, 
              "title":"实验一：业务流程建模",
              "score": 91, 
                  {
                  "evaluate_id":001,
                  "title":"内容是否完整",
                  "score":95,
                  "comment":"内容很完整",
                  "weight":0.4
                  }
                  {
                  ...其他评分项
                  }
              "update_date": "2018-04-02 13:48:01"
              }, 
              {
              ...其他实验
              }
          ] 
    }
* 返回参数说明：

|参数名称|说明|
|:---:|:---:|
|status|bool类型，true表示正确的返回，false表示有错误|
|info|返回结果说明信息|
|student_id|学号|
|github_username|学生的gitHub用户名|
|class|班级|
|name|真实姓名|
|total|实验总数|
|avgresult|实验平均成绩|
|data|所有实验的成绩和评语|
|test_id|实验编号|
|web_exists|本实验的GitHub网页是否存在|
|title|实验标题|
|score|实验得分|
|evaluate_id|评语编号|
|title|评语标题|
|score|评语得分|
|comment|评价内容|
|weight|该评语在该实验的权重|
|update_date|本实验老师的批改日期，可以为空|
