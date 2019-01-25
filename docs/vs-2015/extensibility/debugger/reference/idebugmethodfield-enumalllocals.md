---
title: IDebugMethodField::EnumAllLocals | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugMethodField::EnumAllLocals
helpviewer_keywords:
- IDebugMethodField::EnumAllLocals method
ms.assetid: 0bc7cc13-2628-4bd8-8c06-4d2aa6755ea8
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 2f0f89c3fee45d6d56b845753958d697e41ab11f
ms.sourcegitcommit: c496a77add807ba4a29ee6a424b44a5de89025ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54833758"
---
# <a name="idebugmethodfieldenumalllocals"></a>IDebugMethodField::EnumAllLocals
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Yöntemi dahili olarak bir derleyici tarafından oluşturulan dahil olmak üzere tüm yerel değişkenlerin için bir numaralandırıcı oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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
