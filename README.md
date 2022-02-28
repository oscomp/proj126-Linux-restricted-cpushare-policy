# proj126-Linux-restricted-cpushare-policy
### 项目名称
限制CFS调度器的CPU并发度

### 项目描述

在Linux CFS 调度器中，当任务被唤醒时有优先使用空闲CPU的倾向。这样设计可以更充分使用CPU资源，避免不必要的排队等待，提供更好的CPU性能。然而当任务允许使用的CPU资源有限时，这种优先使用空闲CPU的设计带来了一些问题。

使用Cgroup [CPUSETS](https://www.kernel.org/doc/html/latest/admin-guide/cgroup-v1/cpusets.html#id2)技术可以设置CPU亲和性，把任务限定到部分CPU上。出于CPU管理成本和使用成本方面的考虑，更广泛的应用场景里采用默认的不设置CPU亲和性策略，出现了限制CFS调度的CPU并发度的需求。

本项目旨在为CFS调度器增加限制Cgroup任务使用CPU的并发度功能。

### 所属赛道

2022全国大学生操作系统比赛的“OS功能挑战”赛道


### 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生（2021年春季学期或之后本科毕业的大一~大四的学生）
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2022全国大学生操作系统比赛”的章程和技术方案要求



### 项目导师

常怀鑫

* github https://github.com/changhuaixin 
* email huaixin.chx@alibaba-inc.com


### 难度

中


### 特征

* Linux CFS调度器优化


### 文档


### License

* [GPL-2.0](https://opensource.org/licenses/GPL-2.0)


## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

* 当负载只有一组时，限制负载使用CPU的并发度。
*  当负载有多组存在CPU竞争时，限制负载使用CPU的并发度，并且避免将多组任务限制到相同CPU上。
