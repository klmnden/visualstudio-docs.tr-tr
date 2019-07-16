---
title: IDebugSettingsCallback2::EnumEEs | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugSettingsCallback2::EnumEEs
ms.assetid: 9f884c49-426f-461b-b547-9d909486e73f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2cca998c4cdae8cc5e543a24a5cdfe18369e51b3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68155219"
---
# <a name="idebugsettingscallback2enumees"></a>IDebugSettingsCallback2::EnumEEs
Dil ve satıcı tanımlayıcıları verilen kullanılabilir ifade değerlendiricilerini numaralandırır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumEEs(
   DWORD  celtBuffer,
   GUID*  rgguidLang,
   GUID*  rgguidVendor,
   DWORD* pceltEEs
);
```

```csharp
public int EnumEEs(
   uint       celtBuffer,
   ref Guid   rgguidLang,
   ref Guid   rgguidVendor,
   ref uint[] pceltEEs
);
```

#### <a name="parameters"></a>Parametreler
 `celtBuffer`

 [in] İçindeki öğelerin sayısını `pceltEEs` arabellek.

 `rgguidLang`

 [out içinde] Programlama dili için benzersiz tanımlayıcı.

 `rgguidVendor`

 [out içinde] Satıcı için benzersiz tanımlayıcı.

 `pceltEEs`

 [out içinde] İfade değerlendiricilerini dizisi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugSettingsCallback2](../../../extensibility/debugger/reference/idebugsettingscallback2.md)