---
title: IDebugSymbolProvider::GetNamespacesUsedAtAddress | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugSymbolProvider::GetNamespacesUsedAtAddress
helpviewer_keywords:
- IDebugSymbolProvider::GetNamespacesUsedAtAddress method
ms.assetid: 392de54b-9af0-4567-953b-1b41acd1e05c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: fc32ea0d07779f82bb741b99632ec16a950e5da2
ms.sourcegitcommit: 6196d0b7fdcb08ba6d28a8151ad36b8d1139f2cc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65223966"
---
# <a name="idebugsymbolprovidergetnamespacesusedataddress"></a>IDebugSymbolProvider::GetNamespacesUsedAtAddress
Bu yöntem hata ayıklama adresiyle ilişkili ad alanları için bir numaralandırıcı oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetNamespacesUsedAtAddress( 
   IDebugAddress*     pAddress,
   IEnumDebugFields** ppEnum
);
```

```csharp
int GetNamespacesUsedAtAddress(
   IDebugAddress        pAddress,
   out IEnumDebugFields ppEnum
);
```

## <a name="parameters"></a>Parametreler
 `pAddress`\

 [in] Hata ayıklama adresi.

 `ppEnum`\

 [out] Döndürür bir [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) ad alanları için bir numaralandırıcı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Olabilir verilen hata ayıklama adresi ile Örneğin, ilişkili çeşitli ad alanları ad alanları veya birden çok iç içe geçmiş `using` deyimleri.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)
- [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)