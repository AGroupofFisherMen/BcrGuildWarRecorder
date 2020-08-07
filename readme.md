

---
### 接口设计


---

### 数据库结构

##### 用户表 users

| 参数名称   | 参数类型 | 参数说明 |
| ------ | ----- | ------------ |
| account | string | 账号 |
| gameid | string() | 游戏内的id |
| username | string(16) | 用户名（游戏内的） |
| password | string | 密码 |
| ismember | bool | 是否是工会成员（方便会员跑路） |
| manager | bool | 是否管理 |

> 是否是管理这个可以不要，因为可以写死管理员登陆信息到代码里

##### 目标设置表 targetsetting

| 参数名称   | 参数类型 | 参数说明 |
| ------ | ----- | ------------ |
| battletime | int(6) | 会战时间(YYYYDD) |
| bossround | int(2) | boss轮数 |
| bossnum | int(1) | boss位数（第几个boss） |
| damage | int(8) | （目标）出刀伤害 |
| multiply | float | 记分系数 |

##### 伤害表 damage

| 参数名称   | 参数类型 | 参数说明 |
| ------ | ----- | ------------ |
| gameid | int() | 游戏内的id |
| battletime | int(6) | 会战时间(YYYYDD) |
| damage | int(8) | 出刀伤害 |
| attacktime | time | 出刀时间 |
| bossround | int(2) | boss轮数 |
| bossnum | int(1) | boss位数（第几个boss）|

##### 日志表 log

| 参数名称   | 参数类型 | 参数说明 |
| ------ | ----- | ------------ |
| account | string | 操作账号 |
| operatingtime | time | 操作时间 |
| message | string | 日志 |