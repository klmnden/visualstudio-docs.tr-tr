---
title: IDebugSymbolProvider::GetNextAddress | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugSymbolProvider::GetNextAddress
helpviewer_keywords:
- IDebugSymbolProvider::GetNextAddress method
ms.assetid: 704eeb94-cb13-49d1-82b6-7d83ed0f19c0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 574111db390388ee1d0c572a3a8825c3a2ae9469
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56722765"
---
# <a name="idebugsymbolprovidergetnextaddress"></a>IDebugSymbolProvider::GetNextAddress
Bir yöntemde belirli hata ayıklama adresi aşağıdaki hata ayıklama adresi alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetNextAddress( 
   IDebugAddress*  pAddress,
   BOOL            fStatementOnly,
   IDebugAddress** ppAddress
);
```

```csharp
int GetNextAddress( 
   IDebugAddress     pAddress,
   bool              fStatementOnly,
   out IDebugAddress ppAddress
);
```

#### <a name="parameters"></a>Parametreler
 `pAddress`

 [in] Hata ayıklama adresi verilir.

 `fStatementOnly`

 [in] TRUE ise tek bir deyimde hata ayıklama adresler sınırlar.

 `ppAddress`

 [out] Sonraki hata ayıklama adresi döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Geçerli bir döndürür `HRESULT`, genellikle S_OK.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)