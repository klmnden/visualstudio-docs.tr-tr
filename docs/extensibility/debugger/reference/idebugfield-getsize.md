---
title: IDebugField::GetSize | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugField::GetSize
helpviewer_keywords:
- IDebugField::GetSize method
ms.assetid: 73329924-3751-4f44-af54-5986b7943374
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fa10836b91306a99629e80b6869880f018878c38
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56707997"
---
# <a name="idebugfieldgetsize"></a>IDebugField::GetSize
Bu yöntem, bir alanın bayt cinsinden boyutunu alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetSize( 
   DWORD* pdwSize
);
```

```csharp
int GetSize(
   out uint pdwSize
);
```

#### <a name="parameters"></a>Parametreler
 `pdwSize`

 [out] Boyutu döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Tüm alanlar bir türüne sahiptir ve tüm türleri bir boyuta sahiptir. Örneğin, 1 bayt boyutunu bayt türünde bir alan vardır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)