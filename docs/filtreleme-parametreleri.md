---
title: Filtreleme Parametreleri
---
# Filtreleme Parametreleri

### İşlem Parametreleri

Listeleme servislerinde istek sorgusunda kullanılan parametrelerle ilgili detaylar ve örnekler aşağıda belirtilmiştir.

```
{
    "filters":"",
    "params" :"",
    "limit":"1000",
    "offset" : "0",
    "sorting":[{"field": "id", "sort": "ASC"}]
}
```

| Tag | Açıklama |
| --- | --- |
| `filters` | Listelemek istediğiniz kolon veya belirli bir veriyi çekebilmek için kullanılabilen filtreleme alanıdır. |
| `params` | Listelenecek kolonları ifade eder. |
| `limit*` | Listelemek istediğiniz veri sayısını ifade eder. |
| `offset*` | Listelemek istediğiniz veri işlem numarasının (id) başlangıç değerini ifade eder. |
| `sorting` | Listelemek istediğiniz verilerin sıralama standardını ifade eder. |

{% hint style="info" %} limit ve offset parametreleri zorunlu parametrelerdir. {% endhint %}

Filtreleme Örneği

Filters alanı kullanarak istenilen bir kolonda belirlenen veriye uygun kaydın getirilmesi istenmektedir.

```
{
    "filters":[{"field": "id", "operator": "=", "value":"1"}],
    "params" :"",
    "limit":"",
    "offset" : "",
    "sorting":""
}
```

| Tag | Açıklama | Format |
| --- | --- | --- |
| field | Listelemek istediğimiz verilerin ait olduğu kolonları ifade eder. | **String** |
| operator | Field ve value değerleri arasındaki eşleştirme ifadelerini parametre olarak alır. | **"=", "OR =", ">", "OR >", "<", "<=", "OR <", ">=", "OR >=", "<=", "OR <=", "<>", "OR <>", "IN", "OR IN", "NOT LIKE", "NOT IN", "OR NOT IN", "LIKE", "OR LIKE", "OR NOT LIKE", "LIKE AFTER", "LIKE BEFORE", "LIKE NONE"** |

Filtreleme Örneği 2

Params alanı kullanılarak listelenecek alanlar arasında yalnızca "id" kolonunun listelenmesi beklenmektedir.

```
{
    "filters":"",
    "params" : {"colums": ["id"]},
    "limit":"",
    "offset" : "",
    "sorting":""
}
```

| Tag | Açıklama | Format |     |
| --- | --- | --- | --- |
| colums | Listelemek istediğiniz kolonları ifade eder. | **String** |     |

Filtreleme Örneği 3

Limit alanı kullanılarak listeden belirtilen sayı miktarınca kayıt listelenmesi beklenmektedir.

```
{
    "filters":"",
    "params" : "",
    "limit":"100",
    "offset" : "",
    "sorting":""
}
```

Filtreleme Örneği 3

Offset alanı kullanılarak listelenecek verilerin tablo pk id numarasının belirtilen değerden başlanarak listelenmesi beklenmektedir.

```php
{
    "filters":"",
    "params" : "",
    "limit":"",
    "offset" : "0",
    "sorting":""
}
```

Filtreleme Örneği 4

Sorting alanı kullanılarak listelenecek verilerin belirlenen bir sıralama dahilinde listelenmesi beklenmektedir.

```
{
    "filters":"",
    "params" :"",
    "limit":"",
    "offset" : "",
    "sorting":[{"field": "id", "sort": "ASC"}]
}
```

| Tag | Açıklama | Format |
| --- | --- | --- |
| field | Listelemek istediğimiz verilerin ait olduğu kolonları ifade eder. | **String** |
| sort | Listelemek istediğimiz verilerin hangi sıralama formatı ile sıralanacağını ifade eder. | **"asc", "desc"** |