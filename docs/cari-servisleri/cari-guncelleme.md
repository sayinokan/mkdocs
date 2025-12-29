---
title: Cari Güncelleme
---
# Cari Güncelleme

### URL

| HTTP Metod | URL |
| --- | --- |
| `POST` | `https://www.siteadi.com/api/v1/customer/customer_update` |

### İşlem Parametreleri[](#url)

Cari güncelleme işlemi için isteklerde gönderilmesi beklenen parametreler ve sorgu örneği aşağıda belirtilmiştir.

```
{
"column":{ 
            "id": "1",
            "name": "Test Carisi",
            "customer_type_1": "2",
            "customer_type_2": "1",
            "status": "1", 
            "tax_department": "",
            "tax_number": "",
            "tc_number": "",
            "group_code": "",
            "branch_key": "0",
            "branch_name": "",
            "telephone": "000000000000000",
            "email": "test@oduyo.com.tr",
            "country": "",
            "province": "",
            "district": "",
            "risk": "",
            "balance": "-9440.0000",
            "balance_current": "0.0000",
            "balance_paid": "0.0000"
         }
}
```

| Tag | Açıklama | Format |
| --- | --- | --- |
| ```<br>id<br>``` | Güncellenecek Tablo Pk İd | **Numerik(int)** |
| ```<br>name<br>``` | Cari Adı | **String** |
| ```<br>customer_type_1<br>``` | Cari Türü | **"1"="şahıs", "2"="kuruluş",** |
| ```<br>customer_type_2<br>``` | Cari Türü | **'Alıcı'=>'1', 'Satıcı'=>'2', 'Alıcı + Satıcı'=>'3'** |
| ```<br>status<br>``` | Cari Aktiflik Durumu | **Numerik** |
| ```<br>tax_department<br>``` | Vergi Dairesi | **String** |
| ```<br>tax_number<br>``` | Vergi Numarası | **String** |
| ```<br>tc_number<br>``` | T.C Numarası | **String** |
| ```<br>group_code<br>``` | ERP Grup Kodu | **String** |
| ```<br>branch_key<br>``` | ERP Şube Kodu | **String** |
| ```<br>branch_name<br>``` | Şube Adı | **String** |
| ```<br>telephone<br>``` | Telefon Numarası | **String** |
| ```<br>email<br>``` | E-Posta Adresi | **String** |
| ```<br>country<br>``` | Ülke | **String** |
| ```<br>province<br>``` | İl  | **String** |
| ```<br>district<br>``` | İlçe | **String** |
| ```<br>risk<br>``` |     | **String** |
| ```<br>balance*<br>``` | Cari Bakiye | **Numerik(decimal)** |
| ```<br>balance_current*<br>``` | Vadesi Gelen Bakiye | **Numerik(decimal)** |
| ```<br>balance_paid*<br>``` | Toplam Ödenen Bakiye | **Numerik(decimal)** |

## Cari Güncelleme

`POST` `https://www.siteadi.com/api/v1/customer/customer_update`

Ödüyo içerisine gönderilen cari bilgilerini günceller.

#### Headers

| Name | Type | Description |
| --- | --- | --- |
| Apikey\* | String | Ödüyo paneli içerinde APIKEY bölümünden alınmalıdır. |
| Authorization\* | String | Kullanıcı denetimi bölümünde anlatılan Login servisi ile üretilmelidir. (SESSION\_ID) |

#### Request Body

| Name | Type | Description |
| --- | --- | --- |
| name | string | Cari Adı |
| customer\_type\_1 | string | Cari Türü |
| id\* | numeric(int) | Güncellenecek Tablo Pk İd |
| customer\_type\_2 | string | Cari Türü |
| status | string | Cari Aktiflik Durumu |
| tax\_department | string | Vergi Dairesi |
| tax\_number | string | Vergi Numarası |
| tc\_number | string | T.C Numarası |
| group\_code | string | ERP Grup Kodu |
| branch\_key | string | ERP Şube Kodu |
| branch\_name | string | Şube Adı |
| telephone | string | Telefon Numarası |
| email | string | E-Posta Adresi |
| country | string | Ülke |
| province | string | İl  |
| district | string | İlçe |
| balance\* | numeric(decimal) | Cari Bakiye |
| balance\_current\* | numeric(decimal) | Vadesi Gelen Bakiye |
| balance\_paid\* | numeric(decimal) | Toplam Ödenen Bakiye |

\=== "200 Başarılı" `javascript { "status": true, "data": "<1> successfully updated." }` \=== "400: Bad Request Hatalı" `{ }`

!!! info **Önemli:** Header içerisinde mutlaka Apikey ve Session ID bilgisi gönderilmelidir.