---
title: SccGetExtendedCapabilities işlevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccGetExtendedCapabilities
helpviewer_keywords:
- SccGetExtendedCapabilities function
ms.assetid: 588c6a92-2147-4d8b-a357-96ca7da0a092
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9ed27c996a94c4e81a946efbfa2684dc4169005a
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56720477"
---
# <a name="sccgetextendedcapabilities-function"></a>SccGetExtendedCapabilities işlevi
Bu işlev, kaynak denetimi eklentisi tarafından desteklenen ek özellikleri döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
SCCRTN SccGetExtendedCapabilities(
   LPVOID pContext,
   LONG lSccExCaps,
   LPBOOL pbSupported
);
```

### <a name="parameters"></a>Parametreler
 pContext

[in] Kaynak Denetimi Eklentisi bağlam işaretçisi.

 lSccExCaps

[in] Test etmek istediğiniz genişletilmiş bir özellik belirten bir bayrak (genişletilmiş özelliği kodu tablosuna bakın [özellik bayrakları](../extensibility/capability-flags.md) olası bayrakları için).

 pbSupported

[out] Sıfır olmayan döndürür (`TRUE`) belirtilen yeteneği desteklenir; Aksi takdirde, sıfır döndürür (`FALSE`).

## <a name="return-value"></a>Dönüş değeri
 Kaynak Denetimi Eklentisi uygulanması bu işlev, aşağıdaki değerlerden birini döndürmesi beklenir:

|Değer|Açıklama|
|-----------|-----------------|
|SCC_OK|Alma özelliği işlemi başarıyla tamamlandı.|
|SCC_E_UNKNOWNERROR<br /><br /> SCC_E_NONSPECIFICERROR|Bilinmeyen veya belirtilmeyen bir hata oluştu.|

## <a name="remarks"></a>Açıklamalar
 İsteğe bağlı olarak bu yöntem çağrılır; Test edilecek bir yetenek gerektiğinde, diğer bir deyişle, bu yöntem belirlemek için özellik desteklenen çağrılır. Aynı anda yalnızca bir bayrağı belirtilmiş.

## <a name="see-also"></a>Ayrıca bkz.
- [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md)
- [Hata kodları](../extensibility/error-codes.md)
- [Özellik bayrakları](../extensibility/capability-flags.md)