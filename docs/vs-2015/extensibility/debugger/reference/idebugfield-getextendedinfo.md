---
title: IDebugField::GetExtendedInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugField::GetExtendedInfo
helpviewer_keywords:
- IDebugField::GetExtendedInfo method
ms.assetid: 46c0dd4d-4fd5-4efd-a908-71e4248e8e8d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3de21bc984a36db87f8ce1567f4ff7d97212c40e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62547565"
---
# <a name="idebugfieldgetextendedinfo"></a>IDebugField::GetExtendedInfo
Bu yöntem, bir alan hakkında bilgi genişletilmiş.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetExtendedInfo( 
   REFGUID guidExtendedInfo,
   BYTE**  prgBuffer,
   DWORD*  pdwLen
);
```

```csharp
int GetExtendedInfo(
   ref Guid guidExtendedInfo,
   IntPtr[] prgBuffer,
   ref uint pdwLen
);
```

#### <a name="parameters"></a>Parametreler
 `guidExtendedInfo`

 [in] Döndürülecek bilgileri seçer. Geçerli değerler şunlardır:

|Değer|Açıklama|
|-----------|-----------------|
|`guidConstantValue`|Bayt dizisi olarak değeri.|
|`guidConstantType`|Tür imzası olarak türü.|

 `prgBuffer`

 [out] Genişletilmiş bilgileri döndürür.

 `pdwLen`

 [out içinde] Genişletilmiş bilgileri boyutunu bayt cinsinden döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Şu anda, bu yöntem, yalnızca türe veya bir sabit değerini döndürür. Çağırana döndürülen arabellek boşaltmanız gerekir `prgBuffer` COM'ın çağırarak `CoTaskMemFree` işlevi (C++) veya <xref:System.Runtime.InteropServices.Marshal.FreeCoTaskMem%2A> (C#).

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)