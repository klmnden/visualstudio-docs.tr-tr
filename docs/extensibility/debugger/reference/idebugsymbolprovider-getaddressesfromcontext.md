---
title: IDebugSymbolProvider::GetAddressesFromContext | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugSymbolProvider::GetAddressesFromContext
helpviewer_keywords:
- IDebugSymbolProvider::GetAddressesFromContext method
ms.assetid: a3124883-a255-4543-a5ec-e1c7a97beb69
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a7b28010f117b1bb6616250f1e188bd5acb38cda
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62915866"
---
# <a name="idebugsymbolprovidergetaddressesfromcontext"></a>IDebugSymbolProvider::GetAddressesFromContext
Bu yöntem, bir belge bağlamına bir hata ayıklama adresleri dizisine eşler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetAddressesFromContext( 
   IDebugDocumentContext2* pDocContext,
   BOOL                    fStatmentOnly,
   IEnumDebugAddresses**   ppEnumBegAddresses,
   IEnumDebugAddresses**   ppEnumEndAddresses
);
```

```csharp
int GetAddressesFromContext(
   IDebugDocumentContext2  pDocContext,
   bool                    fStatmentOnly,
   out IEnumDebugAddresses ppEnumBegAddresses,
   out IEnumDebugAddresses ppEnumEndAddresses
);
```

#### <a name="parameters"></a>Parametreler
 `pDocContext`

 [in] Belge bağlamı.

 `fStatmentOnly`

 [in] TRUE ise tek bir deyimde hata ayıklama adresler sınırlar.

 `ppEnumBegAddresses`

 [out] Bu deyim veya satır ile ilişkili başlangıç hata ayıklama adresi için bir numaralandırıcı döndürür.

 `ppEnumEndAddresses`

 [out] Döndürür bir [IEnumDebugAddresses](../../../extensibility/debugger/reference/ienumdebugaddresses.md) bu deyimi veya satır ile ilişkili bitiş hata ayıklama adresi için bir numaralandırıcı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir belge bağlamına genellikle bir dizi kaynak satırları gösterir. Bu yöntem, başlangıç sağlar ve bitiş adreslerini hata ayıklama bu satırlar ile ilişkili. Bazı diller, birden fazla satır ya da birden fazla deyim içeren satırları span deyimleri sağlar. Bu yöntem, tek bir deyimde hata ayıklama adresler sınırlamak için bir bayrak sağlar.

 Tek bir deyimde şablonları olduğu gibi birden çok hata ayıklama adresi olması mümkündür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)
- [GetAddressesFromPosition](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromposition.md)
- [IEnumDebugAddresses](../../../extensibility/debugger/reference/ienumdebugaddresses.md)