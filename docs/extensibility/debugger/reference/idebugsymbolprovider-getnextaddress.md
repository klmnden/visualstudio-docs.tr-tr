---
title: IDebugSymbolProvider::GetNextAddress | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
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
ms.openlocfilehash: f24871063e39c489761fd527322b40a4be09f6dc
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54949434"
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
 [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)