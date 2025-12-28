---
title: Banka Hesap Güncelleme
---
# Banka Hesap Güncelleme

URL

| HTTP Metod |     |
| --- | --- |
| POST | https://www.siteadi.com/api/v1/erp/erp\_bank\_account/update |

#### İşlem Parametreleri[](#url-1)

```
{
"column":{ 
            "id" :121,
            "integration_id": "2", 
            "status": "1", 
            "currency": "TL",
            "account_no": "0960900010100046", 
            "iban": "TR660006701000000093520111",
            "account_name": "Akbank T.A.Ş.", 
            "account_code": "1000104", 
            "account_branch": "0609",
            "banka_key": "770-80-011",
            "space1":"",
            "space2":"",
            "space3":"",
            "space4":"",
            "space5":"",
            "note":"",
            "hhs_code":"",
            "hhs_code_desc":"",
            "tckn_area":"",
            "name":"",
            "phone_area":"",
            "email_area":""
          }
}
```

Headers

| Name | Type | Description |
| --- | --- | --- |
| Apikey\* | String | Ödüyo paneli içerinde APIKEY bölümünden alınmalıdır. |
| Authorization\* | String | Kullanıcı denetimi bölümünde anlatılan Login servisi ile üretilmelidir. (SESSION\_ID) |

**Request Body**

| Name | Type | Description |
| --- | --- | --- |
| id  | n**umerik(int)** | Hesaba ait Ödüyo id |
| integration\_id | string | Hesaba ait ERP id |
| status | string | Hesap kullanım durumu("1" ⇒ aktif, "0" =>Pasif) |
| currency | string | Hesabın döviz bilgisi |
| account\_no | string | Hesap numarası |
| iban | string | Hesap iban numarası |
| account\_name | string | Hesap adı |
| account\_code | string | Hesap kodu |
| account\_branch | string | Hesap şube numarası |
| banka\_key | string | Hesap Erp kodu |
| space1 | string | Tabloda Yer Alan Ekalan Bilgileri |
| space2 | string | Tabloda Yer Alan Ekalan Bilgileri |
| space3 | string | Tabloda Yer Alan Ekalan Bilgileri |
| space4 | string | Tabloda Yer Alan Ekalan Bilgileri |
| space5 | string | Tabloda Yer Alan Ekalan Bilgileri |
| note | string | Hesap açıklama |
| hhs\_code | string | Banka kodu |
| hhs\_code\_desc | string | Banka key |
| tckn\_area | string | Hesabın tanımlı olduğu tckn |
| name | string | Hesaba ait ad soyad |
| phone\_area | string | Bildirim tel no |
| email\_area | string | Bildirim mail adresi |

\=== "200" `{ "status": true, "data": "Guncelleme islemi Basarili" }` \=== "404" `{ "status": false }`