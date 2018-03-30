# 业务流程建模
| 学号 | 班级 | 姓名 | 照片|
|:----:|:-----:|:----:|:----:|
| 201510414320 | 软件（本）15-3 | 谢超 | [![]() |

## 图6.1：考试及成绩管理流程
### PlantUML源码如下：
    @startuml
    |教务处|
    start
    :安排考试;
    :考试安排表]
    |#AntiqueWhite|教师|
    :出卷;
    fork
        :A、B试卷|
    fork again
        :打印审批表]
    |#AntiqueWhite|系主任|
        :审批签字;
        :打印审批表;
    end fork
    |#AntiqueWhite|教务处|
    :打印试卷;
    :试卷]
    |#AntiqueWhite|学生|
    :参加考试;
    :答卷]
    |#AntiqueWhite|教师|
    :阅读出成绩;
    fork
        :成绩单]
    |#AntiqueWhite|教务处|
    if (有不及格) then (有)
        fork
        :安排补考;
        :补考安排表]
        detach
        end fork
    endif
    |#AntiqueWhite|教师|
    fork again
        :答卷]
        :装订存档;
    end fork
    :期末流程结束;
    stop
    @enduml
### 业务流程图如下：
[![](./flow1.png 'flow1')](./flow1.png)


## 图6.2：客户维修服务流程
### PlantUML源码如下：
    @startuml
    |客户|
    start
    :申请服务;
    |#AntiqueWhite|业务经理|
    if (是新客户吗？) then (是)
        :登记客户信息;
    else (不是)
    endif
    :上门勘察;
    :制定方案;
    |#AntiqueWhite|客户|
    if (满意吗？) then (否)
        stop
    else (是)
        :签订服务合同;
    endif
    |#AntiqueWhite|业务经理|
    fork
        :安排工人;
    fork again
        :安排材料;
    end fork
    :填写派工单;
    |#AntiqueWhite|工人|
    :领取材料;
    :上门服务;
    |#AntiqueWhite|客户|
    :验收并填写反馈意见;
    |#AntiqueWhite|业务经理|
    :交回派工单;
    |#AntiqueWhite|财务人员|
    :结束收款;
    stop
    @enduml
### 业务流程图如下：
[![](./flow2.png '百度')](./flow2.png)