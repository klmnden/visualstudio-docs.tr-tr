---
title: IDebugMethodField::EnumAllLocals | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugMethodField::EnumAllLocals
helpviewer_keywords:
- IDebugMethodField::EnumAllLocals method
ms.assetid: 0bc7cc13-2628-4bd8-8c06-4d2aa6755ea8
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 5f03a285a390e244babe99b2cc0ae2db5bf9e67f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53846288"
---
# <a name="idebugmethodfieldenumalllocals"></a>IDebugMethodField::EnumAllLocals
Yöntemi dahili olarak bir derleyici tarafından oluşturulan dahil olmak üzere tüm yerel değişkenlerin için bir numaralandırıcı oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT EnumAllLocals(   
   IDebugAddress*     pAddress,  
   IEnumDebugFields** ppLocals  
);  
```  
  
```csharp  
int EnumAllLocals(  
   IDebugAddress        pAddress,   
   out IEnumDebugFields ppLocals  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pAddress`  
 [in] Bir [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) belirli bir kapsam ya da bağlam işaret eden bir yöntem içinde bir hata ayıklama adresi temsil eden nesne.  
  
 `ppLocals`  
 [out] Döndürür bir [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md) belirtilen kapsamdaki tüm yerel öğeleri listesini temsil eden nesne; Aksi takdirde, hiçbir Yereller belirten bir null değer döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür veya hiçbir yerel öğeler varsa S_FALSE döndürür. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Yalnızca belirli hata ayıklama adresi içeren bir blok içinde tanımlanan değişkenler numaralandırılır. Bu yöntem, tüm derleyici tarafından oluşturulan yerel öğeler içerir. Gerekli tüm çağrı kaynak, açıkça tanımlanmış Yereller varsa [EnumLocals](../../../extensibility/debugger/reference/idebugmethodfield-enumlocals.md) yöntemi.  
  
 Bir yöntem, birden çok kapsam belirleme bağlamları veya blok içerebilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)   
 [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)   
 [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)   
 [EnumLocals](../../../extensibility/debugger/reference/idebugmethodfield-enumlocals.md)