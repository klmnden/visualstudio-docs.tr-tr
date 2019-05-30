---
title: IDebugSymbolProviderDirect::GetMethodFromAddress | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugSymbolProviderDirect::GetMethodFromAddress
- GetMethodFromAddress
ms.assetid: 33ffd197-1221-41bc-a9f6-f133ebdcb783
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 89a110886837c793d45842db6ed80690626dd9d6
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66335162"
---
# <a name="idebugsymbolproviderdirectgetmethodfromaddress"></a>IDebugSymbolProviderDirect::GetMethodFromAddress
Belirtilen hata ayıklama adresindeki yöntem hakkında bilgi alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetMethodFromAddress(
   IDebugAddress* pAddress,
   GUID*          pGuid,
   DWORD*         pAppID,
   _mdToken*      pTokenClass,
   _mdToken*      pTokenMethod,
   DWORD*         pdwOffset,
   DWORD*         pdwVersion
);
```

```csharp
int GetMethodFromAddress(
   IDebugAddress pAddress,
   out Guid      pGuid,
   out uint      pAppID,
   out uint      pTokenClass,
   out uint      pTokenMethod,
   out uint      pdwOffset,
   out uint      pdwVersion
);
```

## <a name="parameters"></a>Parametreler
`pAddress`\
[in] Tarafından temsil edilen adresi hata ayıklama [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi.

`pGuid`\
[out] Modülün benzersiz tanımlayıcısı.

`pAppID`\
[out] Uygulama etki alanı tanımlayıcısı.

`pTokenClass`\
[out] Belirteç, içeren sınıfı temsil eder.

`pTokenMethod`\
[out] Modülü temsil eden belirteç.

`pdwOffset`\
[out] Başından itibaren bayt uzaklığını `pAddress` parametresi.

`pdwVersion`\
[out] Yöntem sürüm numarası.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugSymbolProviderDirect](../../../extensibility/debugger/reference/idebugsymbolproviderdirect.md)