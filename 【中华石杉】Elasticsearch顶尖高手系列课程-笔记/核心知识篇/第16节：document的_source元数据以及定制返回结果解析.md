## ��16�ڣ�document��_sourceԪ�����Լ����Ʒ��ؽ������

### 1��_sourceԪ����

```http request
put /test_index/test_type/1
{
  "test_field1": "test field1",
  "test_field2": "test field2"
}

get /test_index/test_type/1

{
  "_index": "test_index",
  "_type": "test_type",
  "_id": "1",
  "_version": 2,
  "found": true,
  "_source": {
    "test_field1": "test field1",
    "test_field2": "test field2"
  }
}
```



**_sourceԪ����**������˵�������ڴ���һ��document��ʱ��ʹ�õ��Ǹ�����request body�е�json����Ĭ������£���get��ʱ�򣬻�ԭ�ⲻ���ĸ����Ƿ��ػ�����



### 2�����Ʒ��ؽ��

���Ʒ��صĽ����ָ��_source�У�������Щfield

```http request
GET /test_index/test_type/1?_source=test_field1,test_field2

{
  "_index": "test_index",
  "_type": "test_type",
  "_id": "1",
  "_version": 2,
  "found": true,
  "_source": {
    "test_field2": "test field2"
  }
}
```

