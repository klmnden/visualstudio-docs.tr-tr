---
title: IDebugSettingsCallback2::GetEEMetricDword | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugSettingsCallback2::GetEEMetricDword
ms.assetid: c5f8f417-0ef0-4fd0-a779-b0a8ead4effe
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: b3c8349b8a7f7b823d4596f167889a227b166b7a
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65457346"
---
# <a name="idebugsettingscallback2geteemetricdword"></a>IDebugSettingsCallback2::GetEEMetricDword
İfade değerlendirici belirtilen ölçüm için karşılık gelen bir değer alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetEEMetricDword(
   REFGUID guidLang,
   REFGUID guidVendor,
   LPCWSTR pszMetric,
   DWORD*  pdwValue
);
```

```csharp
private int GetEEMetricDword(
   ref Guid guidLang,
   ref Guid guidVendor,
   string   pszMetric,
   out uint pdwValue
);
```

## <a name="parameters"></a>Parametreler
 `guidLang`\

 [in] Programlama diline benzersiz tanımlayıcısı.

 `guidVendor`\

 [in] Satıcı benzersiz tanımlayıcısı.

 `pszMetric`\

 [in] Ölçüm adı.

 `pdwValue`\

 [out] Ölçüm dizesine karşılık gelen bir değer döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugSettingsCallback2](../../../extensibility/debugger/reference/idebugsettingscallback2.md)