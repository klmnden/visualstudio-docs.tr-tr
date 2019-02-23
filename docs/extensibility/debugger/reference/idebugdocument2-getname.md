---
title: IDebugDocument2::GetName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDocument2::GetName
helpviewer_keywords:
- IDebugDocument2::GetName
ms.assetid: 6f09ff09-b0cf-4472-8fc8-143991f0ceb1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3f1ef243afd607a565e2c7a8e6f557f0b9906c86
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56701023"
---
# <a name="idebugdocument2getname"></a>IDebugDocument2::GetName
Belge adını çeşitli biçimlerden birinde alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetName( 
   GETNAME_TYPE gnType,
   BSTR*        pbstrFileName
);
```

```csharp
int GetName( 
   enum_GETNAME_TYPE gnType,
   out string        pbstrFileName
);
```

#### <a name="parameters"></a>Parametreler
 `gnType`

 [in] Bir değer [GETNAME_TYPE](../../../extensibility/debugger/reference/getname-type.md) adı döndürülecek türünü belirleyen sabit listesi.

 `pbstrFileName`

 [out] Belge adını içeren bir dize döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, bir başlık veya bir dosya adı veya hatta bir dosya adının parçası olarak belge adını geri dönebilirsiniz.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugDocument2](../../../extensibility/debugger/reference/idebugdocument2.md)
- [GETNAME_TYPE](../../../extensibility/debugger/reference/getname-type.md)