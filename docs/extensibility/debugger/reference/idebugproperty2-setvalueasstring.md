---
title: IDebugProperty2::SetValueAsString | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProperty2::SetValueAsString
helpviewer_keywords:
- IDebugProperty2::SetValueAsString
ms.assetid: 9e6a5054-41b7-4223-b509-b93689d366a5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: ba8a7ab97c9b2fc405e10eb70246a049b4083993
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66200212"
---
# <a name="idebugproperty2setvalueasstring"></a>IDebugProperty2::SetValueAsString
Belirli bir dizedeki bir özelliğin değerini ayarlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetValueAsString ( 
   LPCOLESTR pszValue,
   UINT      nRadix,
   DWORD     dwTimeout
);
```

```csharp
int SetValueAsString ( 
   string pszValue,
   uint   nRadix,
   uint   dwTimeout
);
```

## <a name="parameters"></a>Parametreler
`pszValue`\
[in] Ayarlanacak değer içeren bir dize.

`nRadix`\
[in] Sayısal yedeklenmesine yorumlama olarak kullanılacak bir sayı tabanı. Bu sayı tabanı otomatik olarak belirlemek girişiminde 0 olabilir.

`dwTimeout`\
[in] Bu yöntemden geri dönmeden önce beklenecek milisaniye cinsinden en uzun süreyi belirtir. Kullanım `INFINITE` süresiz bekleme.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür. Diğer olası değerler aşağıdaki tabloda gösterilmektedir.

|Değer|Açıklama|
|-----------|-----------------|
|`E_SETVALUE_VALUE_CANNOT_BE_SET`|Dize bir özellik değeri dönüştürülemedi veya özellik değeri ayarlanamadı.|
|`E_SETVALUE_VALUE_IS_READONLY`|Özellik salt okunurdur.|

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)