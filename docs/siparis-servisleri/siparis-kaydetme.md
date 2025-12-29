---
title: Sipariş Kaydetme
---
# Sipariş Kaydetme

### URL

| HTTP Metod | URL |
| --- | --- |
| `POST` | https://www.siteadi.com/api/v1/order/order\_create |

### İşlem Parametreleri

Sipariş kaydetme işlemi için isteklerde gönderilmesi beklenen parametreler ve sorgu örneği aşağıda belirtilmiştir.

```postman_json
{
"column":{ 
            "customer_id": "2", 
            "status": "1", 
            "title": "Ödüyo Test Carisi",
            "sku": "120.001.001", 
            "order_status": "",
            "average_expiry_date": "10000000146", 
            "total": "1.00", 
            "currency_type": "TL",
            "currency_value": "1.00",
            "parent_process": "0", 
            "parent_process_txt": "", 
            "branch_id": "1",
            "branch_name": "Merkez",
            "storage_id": "1",
            "storage_name": "Ana Depo",
            "order_currency_type": "TL",
            "erp_ref_id": "5",
            "space1":"",
            "space2":"",
            "space3":"",
            "space4":"",
            "space5":"",
            "order_created_in": "2023-10-01 19:30:00",
            "order_updated_in": "2023-10-01 19:30:00", 
            "order_date": "2023-10-06",
            "order_time": "19:00:00",
            "created_in":"2023-10-01 19:30:00",
            "updated_in": "2023-10-01 19:30:00"
}
}
```

## Sipariş Kaydetme

`POST` `https://www.siteadi.com/api/v1/order/order_create`

Ödüyo içerisine gönderilen sipariş işlemlerini kaydeder.

#### Headers

| Name | Type | Description |
| --- | --- | --- |
| Apikey\* | String | Ödüyo paneli içerinde APIKEY bölümünden alınmalıdır. |
| Authorization\* | String | Kullanıcı denetimi bölümünde anlatılan Login servisi ile üretilmelidir. (SESSION\_ID) |

#### Request Body

| Name | Type | Description |
| --- | --- | --- |
| sku\* | varchar | cari hesap kodu |
| order\_status\* | varchar | Sipariş durumu |
| average\_expiry\_date\* | datetime | Sipariş vade tarihi |
| total\* | decimal | Sipariş tutarı |
| currency\_type | varchar | Sipariş para birimi |
| currency\_value | decimal | Sipariş tutarı |
| title\* | varchar | Cari unvan |
| status\* | numeric(int) | Fatura durumu(0-1) |
| customer\_id | numeric(int) | Ödüyo cari id |
| order\_currency\_type | varchar | Sipariş para birimi |
| space1 | text | ekalan |
| branch\_id | varchar | Erp şube id |
| branch\_name | varchar | Erp şube |
| storage\_id | varchar | Erp malzeme id |
| storage\_name | varchar | Erp malzeme adı |
| space2 | text | ekalan |
| space3 | text | ekalan |
| parent\_process | varchar | Üst işlem id |
| parent\_process\_txt | varchar | Üst işlem detayı |
| erp\_ref\_id | varchar | Erp id |
| space4 | text | ekalan |
| order\_created\_in | datetime | Sipariş oluşturulma tarihi |
| order\_updated\_in | datetime | Sipariş güncellenme tarihi |
| invoice\_date | datetime | Sipariş tarihi |
| invoice\_time | datetime | Sipariş saati |
| space5 | text | ekalan |
| order\_date | String | Sipariş tarihi |
| order\_time | String | Sipariş saati |

\=== "200 Başarılı"

````
```javascript
{
"status": true,
"data": "Payment successfully added id <id>"
}
```
````

\=== "400: Bad Request Hatalı"

````
```
{
}
```
````

!!! info **Önemli:** Header içerisinde mutlaka Apikey ve Session ID bilgisi gönderilmelidir.