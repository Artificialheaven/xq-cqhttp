# 信息下报

## 私聊消息

### 事件数据

| 字段名 | 数据类型 | 可能的值 | 说明 |
| ----- | ----- | ----- |----- |
| time | num | ?? | 收到信息的时间戳 |
| self_id | num | ?? | 收到信息的机器人QQ（需先向机器人发送一条信息获取自身QQ） |
| post_type | str | message | 上报类型 |
| message_type | str | private | 信息类型 |
| user_id | num | friend (only) | 信息子类型 |
| message | str | - | 信息内容 |
| raw_message | str | - | 原始信息内容（16进制） |
| font | num | - | 字体（恒为0） |
| sender | json | - | 发送人信息 |

其中的 *sender* 字段内容如下（并不一定完整）

| 字段名 | 数据类型 | 可能的值 | 说明 |
| ----- | ----- | ----- | ----- |
| user_id | num | ？？ | 发送者QQ |

## 群消息

### 消息数据

| 字段名 | 数据类型 | 可能的值 | 说明 |
| ----- | ----- | ----- |----- |
| time | num | ?? | 收到信息的时间戳 |
| self_id | num | ?? | 收到信息的机器人QQ（需先向机器人发送一条信息获取自身QQ） |
| post_type | str | message | 上报类型 |
| message_type | str |group | 信息类型 |
| user_id | num | group (only) | 信息子类型 |
| message | str | - | 信息内容 |
| raw_message | str | - | 原始信息内容（16进制） |
| font | num | - | 字体（恒为0） |
| sender | json | - | 发送人信息 |

其中的 *sender* 字段内容如下（并不一定完整）

| 字段名 | 数据类型 | 可能的值 | 说明 |
| ----- | ----- | ----- | ----- |
| user_id | num | ？？ | 发送者QQ |

### 讨论组事件

*不接受讨论组事件（不确定性）*

## 特殊问题

*在出现不能解析的数据时，返回ERROR*