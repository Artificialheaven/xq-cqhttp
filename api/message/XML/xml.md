# XML的发送

## 发送至私聊

### 参数

| 字段名 | 数据类型 | 可能的值 | 说明 |
| action | str | send_private_xml | 发送至私聊 |
| message_type | str | private | 信息类型 |
| user_id | str/num | - | 用户QQ号 |
| xml_data | str(bin) | - | 文本类型的字节集数据（xml数据） |
| xml_type | str（num）/num | 0、2 | 0：基本、2：点歌 |

*发送至私聊还是群聊主要根据message_type的内容，而不是action*

## 发送至群聊

### 参数

| 字段名 | 数据类型 | 可能的值 | 说明 |
| action | str | send_group_xml | 发送至私聊 |
| message_type | str | group | 信息类型 |
| group_id | str/num | - | 群号 |
| xml_data | str(bin) | - | 文本类型的字节集数据（xml数据） |
| xml_type | str（num）/num | 0、2 | 0：基本、2：点歌 |