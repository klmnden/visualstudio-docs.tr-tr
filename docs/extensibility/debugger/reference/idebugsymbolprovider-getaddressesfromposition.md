---
title: IDebugSymbolProvider::GetAddressesFromPosition | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugSymbolProvider::GetAddressesFromPosition
helpviewer_keywords:
- IDebugSymbolProvider::GetAddressesFromPosition method
ms.assetid: 1b0f02cb-8ace-4614-88f3-0e10239012b3
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 1276a1c1a076c624ffcfd78c3b7f9d09df2a6e01
ms.sourcegitcommit: 6196d0b7fdcb08ba6d28a8151ad36b8d1139f2cc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65224017"
---
# <a name="idebugsymbolprovidergetaddressesfromposition"></a>IDebugSymbolProvider::GetAddressesFromPosition
Bu yöntem, hata ayıklama adresleri dizisine bir belge konumu eşler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetAddressesFromPosition( 
   IDebugDocumentPosition2* pDocPos,
   BOOL                     fStatmentOnly,
   IEnumDebugAddresses**    ppEnumBegAddresses,
   IEnumDebugAddresses**    ppEnumEndAddresses
);
```

```csharp
int GetAddressesFromPosition( 
   IDebugDocumentPosition2  pDocPos,
   bool                     fStatmentOnly,
   out IEnumDebugAddresses  ppEnumBegAddresses,
   out IEnumDebugAddresses  ppEnumEndAddresses
);
```

## <a name="parameters"></a>Parametreler
 `pDocPos`\

 [in] Belge konumu.

 `fStatmentOnly`\

 [in] TRUE ise tek bir deyimde hata ayıklama adresler sınırlar.

 `ppEnumBegAddresses`\

 [out] Bu deyim veya satır ile ilişkili başlangıç hata ayıklama adresi için bir numaralandırıcı döndürür.

 `ppEnumEndAddresses`\

 [out] Döndürür bir [IEnumDebugAddresses](../../../extensibility/debugger/reference/ienumdebugaddresses.md) bu deyimi veya satır ile ilişkili bitiş hata ayıklama adresi için bir numaralandırıcı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Belge konumu, genellikle bir dizi kaynak satırları gösterir. Bu yöntem, başlangıç sağlar ve bitiş adreslerini hata ayıklama bu satırlar ile ilişkili. Bazı diller, birden fazla satır ya da birden fazla deyim içeren satırları span deyimleri sağlar. Bu yöntem, tek bir deyimde hata ayıklama adresler sınırlamak için bir bayrak sağlar.

 Tek bir deyimde şablonları olduğu gibi birden çok hata ayıklama adresi olması mümkündür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)
- [GetAddressesFromContext](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromcontext.md)
- [IEnumDebugAddresses](../../../extensibility/debugger/reference/ienumdebugaddresses.md)