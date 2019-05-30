---
title: Sccısmulticheckoutenabled işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccIsMultiCheckoutEnabled
helpviewer_keywords:
- SccIsMultiCheckoutEnabled function
ms.assetid: 6721639d-e475-4766-81b5-ee40a280fc70
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 93cbefe716b46b3dd3fe481447612c5c7f65daa3
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353578"
---
# <a name="sccismulticheckoutenabled-function"></a>SccIsMultiCheckoutEnabled İşlevi
Bu işlev, kaynak denetimi eklentisi, bir dosyayı birden çok kullanıma izin verip vermediğini denetler.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccIsMultiCheckoutEnabled(
   LPVOID pContext,
   LPBOOL pbMultiCheckout
);
```

#### <a name="parameters"></a>Parametreler
 pContext

[in] Kaynak Denetimi Eklentisi bağlam yapısı.

 pbMultiCheckout

[out] Bu proje için (birden çok kullanıma desteklenir sıfır olmayan anlamına gelir) birden çok kullanıma etkinleştirilip etkinleştirilmediğini belirtir.

## <a name="return-value"></a>Dönüş Değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|Onay başarılı oldu.|
|SCC_E_NONSPECIFICERROR<br /><br /> SCC_E_UNKNOWNERROR|Belirli olmayan hata oluştu.|

## <a name="remarks"></a>Açıklamalar
 IDE dosyaları aynı anda birden fazla kullanıcı tarafından kullanıma alınabildiğinden, belirlemek için iki denetimler yapar. İlk olarak, kaynak denetim sistemi birden çok kullanıma desteklemesi gerekir. Kaynak Denetimi Eklentisi bu özellik başlatma sırasında belirterek belirtebilirsiniz `SCC_CAP_MULTICHECKOUT`. Bundan sonra ikinci bir onay IDE geçerli proje birden çok kullanıma destekleyip desteklemediğini belirlemek için bu işlevi çağırır. Seçili proje için birden çok kullanıma destekleniyorsa, başarılı bir eklenti döndürür kod ve ayarlar `pbMultiCheckout` için sıfır olmayan (`TRUE`) veya `FALSE`.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentisi API İşlevleri](../extensibility/source-control-plug-in-api-functions.md)