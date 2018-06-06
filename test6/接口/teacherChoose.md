# 接口：teacherChoose
用例：[选课](../用例/用例_选课.md)
* 功能：老师选择课程并创建实验
* 权限： 老师：选择课程供学生选择
* API请求地址： 接口基本地址/v1/api/teacherChoose
* 请求方式 ：POST
* 请求实例：
    {
        "course_id":005,
        "semester_id":181
        "class":3
        "room":"10502"
        "date":星期一7，8节
        "tests_title":"信息系统分析与设计",
        "date":
        [
            {
                "test_title":"业务流程建模",
                "test_score":100,
                "test_weight":0.15,
                {
                    "evaluate_title":"内容是否正确",
                    "evaluate_score":100,
                    "evaluate_weight":0.25
                },
                {
                    ...其他评价
                }
            },
            {
                ...其他实验
            }
        ]
        
    }
* 请求参数说明:

|参数名称|说明|
|:---:|:---:|
|course_id|课程号|
|semester_id|学期号|
|class|班级|
|room|上课教室|
|date|上课时间|
|tests_title|实验课程名称|
|date|传入的数据|
|test_title|实验项目名称|
|test_score|实验项目成绩，100|
|test_weight|实验项目权重|
|evaluate_title|评语名称|
|evaluate_score|评语成绩，100|
|evaluate_weight|评语权重|

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