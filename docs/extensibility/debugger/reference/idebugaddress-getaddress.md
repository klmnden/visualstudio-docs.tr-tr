---
title: IDebugAddress::GetAddress | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugAddress::GetAddress
helpviewer_keywords:
- IDebugAddress:GetAddress method
ms.assetid: 2590387b-5d36-4116-9a75-737957b8898e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e91b90fd54ea70aed729707e927ad2394d756139
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54917685"
---
# <a name="idebugaddressgetaddress"></a>IDebugAddress::GetAddress
Bir nesne ve onun kapsamındaki veya kapsayıcı konumunu tanımlayan bir yapıyı döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetAddress (  
   DEBUG_ADDRESS * pAddress  
);  
```  
  
```csharp  
int GetAddress(  
   DEBUG_ADDRESS[] pAddress  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pAddress`  
 [out içinde] A [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) bu yöntem tarafından girilir yapısının.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) yapısı, ilgili bilgileri ile oturum kaplayacak şekilde bu yönteme geçirilir. Bu bilgileri nasıl yorumlanacağını döndürülen bilgileri ve sembol işleyici türüne bağlıdır. Bkz: [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md) daha fazla ayrıntı için.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [DEBUG_ADDRESS](../../../extensibility/debugger/reference/debug-address.md)