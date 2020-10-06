# 公开api

## 公开api是指非发送信息的可供插件调用的api

### get_login_info

#### 参数

| 字段名 | 数据类型 | 可能的值 | 说明 |
| action | str | get_login_info | 获取在线机器人信息 |

#### 响应参数

| 字段名 | 数据类型 | 可能的值 | 说明 |
| user_id | num | - | 姬气人QQ |
| nickname | str | - | 姬气人QQ昵称 |

*该数据不保证准确性，谨慎调用。*




| 字段名 | 数据类型 | 可能的值 | 说明 |
|  |  |  |  |

### 上传图片

#### 参数

| 字段名 | 数据类型 | 可能的值 | 说明 |
| action | str | upload_pic | - |
| pic_type | str | group/private | - |
| pic_Obje | str | - | 上传该图片所属的群号或QQ |
| pic_Bin | str（bin） | - | 文本类型的字节集数据，图片数据 |
| sign | str | - | 特殊标示，插件自行判断。 |

#### 响应

| 字段名 | 数据类型 | 可能的值 | 说明 |
| Pic_data | str | - | 上传图片的GUID |
| sign | str | - | 特殊标示，与上文一致 |

### 上传语音

#### 参数
| 字段名 | 数据类型 | 可能的值 | 说明 |
| action | str | upload-Voice | - |
| Voice_Type | str | group/private | *请不要返回private！* |
| Voice_Bin | str（bin） | - | 文本类型的字节集数据，图片数据 |
| Voice_Obje | str | - | 上传语音所属的群的群号 |
| sign | str | - | 特殊标示，插件自行判断。 |

#### 响应

| 字段名 | 数据类型 | 可能的值 | 说明 |
| Voice_data | str | - | 上传图片的GUID |
| sign | str | - | 特殊标示，与上文一致 |

## `set_group_kick` 群组踢人

### 参数

| 字段名 | 数据类型 | 默认值 | 说明 |
| ----- | ------- | ----- | --- |
| `group_id` | number | - | 群号 |
| `user_id` | number | - | 要踢的 QQ 号  |
| `reject_add_request` | boolean | `false` | 拒绝此人的加群请求 |

### 响应数据

无

## `set_group_ban` 群组单人禁言

### 参数

| 字段名 | 数据类型 | 默认值 | 说明 |
| ----- | ------- | ----- | --- |
| `group_id` | number | - | 群号 |
| `user_id` | number | - | 要禁言的 QQ 号 |
| `duration` | number | `30 * 60` | 禁言时长，单位秒，0 表示取消禁言 |

### 响应数据

无

## `set_group_whole_ban` 群组全员禁言

### 参数

| 字段名 | 数据类型 | 默认值 | 说明 |
| ----- | ------- | ----- | --- |
| `group_id` | number | - | 群号 |
| `enable` | boolean | `true` | 是否禁言 |

### 响应数据

无

## `set_group_admin` 群组设置管理员

### 参数

| 字段名 | 数据类型 | 默认值 | 说明 |
| ----- | ------- | ----- | --- |
| `group_id` | number | - | 群号 |
| `user_id` | number | - | 要设置管理员的 QQ 号 |
| `enable` | boolean | `true` | true 为设置，false 为取消 |

### 响应数据

无

## `set_group_leave` 退出群组

### 参数

| 字段名 | 数据类型 | 默认值 | 说明 |
| ----- | ------- | ----- | --- |
| `group_id` | number | - | 群号 |
| `is_dismiss` | boolean | `false` | 是否解散，如果登录号是群主，则仅在此项为 true 时能够解散 |

### 响应数据

无

## `set_discuss_leave` 退出讨论组

### 参数

| 字段名 | 数据类型 | 默认值 | 说明 |
| ----- | ------- | ----- | --- |
| `discuss_id` | number | - | 讨论组 ID（正常情况下看不到，需要从讨论组消息上报的数据中获得） |

### 响应数据

无
