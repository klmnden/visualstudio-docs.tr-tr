---
title: Idiaaddressmap::put_imagealign | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaAddressMap::put_imageAlign method
ms.assetid: f9ce875d-c263-43e5-a534-f34c37f9866f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4e07bdd71300ed485862a4a95f1f9cbc06b32772
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63402644"
---
# <a name="idiaaddressmapputimagealign"></a>IDiaAddressMap::put_imageAlign
Resim hizalamasını ayarlar.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT put_imageAlign ( 
   DWORD NewVal
);
```

#### <a name="parameters"></a>Parametreler
 NewVal

[in] Yürütülebilir dosya için yeni görüntü hizalama değeri.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Belirtilen bellek sınırlarını için görüntüleri (yüklenen yürütülebilir dosyalar) hizalanır. Bu hizalama, geçerli sistem mimarisi ve derleme ve bağlama zamanı seçenekleri tarafından etkilenebilir. Resmi hizalaması bayt sınırlarda her zaman olur. Aşağıdaki görüntü hizalama değerler geçerlidir: 1, 2, 4, 8, 16, 32 ve 64 baytlık sınırlar.

 Bir çağrı ile geçerli görüntü hizalama alınabilir [Idiaaddressmap::get_imagealign](../../debugger/debug-interface-access/idiaaddressmap-get-imagealign.md) yöntemi.

> [!NOTE]
> Bu yöntem zamanında resmi zaten yüklü. `put_imageAlign` Yöntemi genellikle görüntünün taşınmış veya değiştirilmiş ve yeni bir hizalama gerekli olduğunda kullanılır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaAddressMap](../../debugger/debug-interface-access/idiaaddressmap.md)
- [IDiaAddressMap::get_imageAlign](../../debugger/debug-interface-access/idiaaddressmap-get-imagealign.md)