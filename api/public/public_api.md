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

