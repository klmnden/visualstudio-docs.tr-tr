---
title: IDebugExpressionEvaluator::Parse | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugExpressionEvaluator::Parse
helpviewer_keywords:
- IDebugExpressionEvaluator::Parse method
ms.assetid: e6e31b3a-63a7-4293-bcda-267eb78dffb6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e232ba0fb13cfdb383d7f63a402b361e296505e2
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54971279"
---
# <a name="idebugexpressionevaluatorparse"></a>IDebugExpressionEvaluator::Parse
Bu yöntem, ayrıştırılmış bir ifade için bir ifade dizeye dönüştürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Parse(   
   LPCOLESTR                upstrExpression,  
   PARSEFLAGS               dwFlags,  
   UINT                     nRadix,  
   BSTR*                    pbstrError,  
   UINT*                    pichError,  
   IDebugParsedExpression** ppParsedExpression  
);  
```  
  
```csharp  
int Parse(  
   string                     upstrExpression,   
   enum_PARSEFLAGS            dwFlags,   
   uint                       nRadix,   
   out string                 pbstrError,   
   out uint                   pichError,   
   out IDebugParsedExpression ppParsedExpression  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `upstrExpression`  
 [in] Ayrıştırılacak ifade dize.  
  
 `dwFlags`  
 [in] Bir koleksiyonu [PARSEFLAGS](../../../extensibility/debugger/reference/parseflags.md) ifade nasıl ayrıştırılacak belirlemek sabitler.  
  
 `nRadix`  
 [in] Sayısal yedeklenmesine yorumlamak için kullanılacak sayı tabanı.  
  
 `pbstrError`  
 [out] Hata, insanlar tarafından okunabilen metin olarak döndürür.  
  
 `pichError`  
 [out] İfade dizesinde hata başlangıcı karakter konumunu döndürür.  
  
 `ppParsedExpression`  
 [out] Döndürür ayrıştırılmış ifadesinde bir [IDebugParsedExpression](../../../extensibility/debugger/reference/idebugparsedexpression.md) nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, Ayrıştırılan bir ifade, gerçek bir değer üretir. Ayrıştırılmış bir ifade başka bir deyişle, bir değere dönüştürülür uyumluluğunun değerlendirilebilmesi hazırdır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugExpressionEvaluator](../../../extensibility/debugger/reference/idebugexpressionevaluator.md)   
 [IDebugParsedExpression](../../../extensibility/debugger/reference/idebugparsedexpression.md)   
 [PARSEFLAGS](../../../extensibility/debugger/reference/parseflags.md)