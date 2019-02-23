---
title: IDebugSymbolProvider::GetLanguage | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugSymbolProvider::GetLanguage
helpviewer_keywords:
- IDebugSymbolProvider::GetLanguage method
ms.assetid: e4142183-3d8b-418f-907f-4ee4c753d8ce
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b20222db9b007fbeee6daf0df1921e4c56744818
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56699632"
---
# <a name="idebugsymbolprovidergetlanguage"></a>IDebugSymbolProvider::GetLanguage
Bu yöntem, hata ayıklama adresten Kodu derlemek için kullanılan dili alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetLanguage( 
   IDebugAddress* pAddress,
   GUID*          pguidLanguage,
   GUID*          pguidLanguageVendor
);
```

```csharp
int GetLanguage(
   IDebugAddress pAddress,
   out Guid      pguidLanguage,
   out Guid      pguidLanguageVendor
);
```

#### <a name="parameters"></a>Parametreler
 `pAddress`

 [in] Bir adres nesnesini temsil ettiği bir [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi.

 `pguidLanguage`

 [out] Döndürür bir `GUID` dili belirtir.

 `pguidLanguageVendor`

 [out] Döndürür bir `GUID` dil satıcı belirtir.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Hata ayıklama altyapısı, doğru bir ifade değerlendiricisi seçmek gereken bilgileri elde etmek için bu yöntemi çağırır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)
- [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)