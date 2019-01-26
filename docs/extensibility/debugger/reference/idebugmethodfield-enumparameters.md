---
title: IDebugMethodField::EnumParameters | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugMethodField::EnumParameters
helpviewer_keywords:
- IDebugMethodField::EnumParameters method
ms.assetid: d77b1197-deb6-4144-8d1b-8b09949ccfac
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6eb2272aff9f02e4de85c5420bd687b059c0e839
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55035451"
---
# <a name="idebugmethodfieldenumparameters"></a>IDebugMethodField::EnumParameters
Yöntem parametreleri için bir numaralandırıcı oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT EnumParameters(   
   IEnumDebugFields** ppParams  
);  
```  
  
```csharp  
int EnumParameters(  
   out IEnumDebugFields ppParams  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppParams`  
 [out] Döndürür bir [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) yöntem için parametrelerin listesini temsil eden nesne; hiç parametre varsa, aksi durumda null değeri döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür veya parametresiz varsa S_FALSE döndürür. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Her öğe bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) farklı parametre türleri temsil eden nesne. Çağrı [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) tam olarak hangi tür parametresi bir nesneyi temsil belirlemek için her bir nesne üzerindeki yöntemi.  
  
 Bir parametre hem değişken adını ve türünü içerir. İlk parametre olarak sınıf yöntemi genellikle "Bu" işaretçisidir.  
  
 Yalnızca bir parametre türleri gereklidir, çağrı [EnumArguments](../../../extensibility/debugger/reference/idebugmethodfield-enumarguments.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)   
 [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)   
 [EnumArguments](../../../extensibility/debugger/reference/idebugmethodfield-enumarguments.md)