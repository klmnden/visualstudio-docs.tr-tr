---
title: IDebugExpressionEvaluator::GetMethodProperty | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugExpressionEvaluator::GetMethodProperty
helpviewer_keywords:
- IDebugExpressionEvaluator::GetMethodProperty method
ms.assetid: c394fe4d-eeb6-4feb-828c-098d84a6f1ba
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 0548cab6892ffc6f6b2db81122b76dfe6642301e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49242976"
---
# <a name="idebugexpressionevaluatorgetmethodproperty"></a>IDebugExpressionEvaluator::GetMethodProperty
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem, yerel öğeler, bağımsız değişkenleri ve diğer bir yöntem özelliklerini içeren bir özellik nesnesi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetMethodProperty(   
   IDebugSymbolProvider* pSymbolProvider,  
   IDebugAddress*        pAddress,  
   IDebugBinder*         pBinder,  
   BOOL                  fIncludeHiddenLocals,  
   IDebugProperty2**     ppProperty  
);  
```  
  
```csharp  
int GetMethodProperty(  
   IDebugSymbolProvider pSymbolProvider,   
   IDebugAddress        pAddress,   
   IDebugBinder         pBinder,   
   int                  fIncludeHiddenLocals,   
   out IDebugProperty2  ppProperty  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pSymbolProvider`  
 [in] Sembol sağlayıcısı kullanılmak üzere ifade olarak bir [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md) nesne.  
  
 `pAddress`  
 [in] Adresi olarak ifade edilen kodda bir [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) yakın içeren çözümleneceği nesne, işlev.  
  
 `pBinder`  
 [in] Bağlayıcı kullanılmak üzere ifade olarak bir [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md) nesne.  
  
 `fIncludeHiddenLocals`  
 [in] Sıfır olmayan (`TRUE`) anlamına gelir; gizli Yereller dahil etmek sıfır (`FALSE`) gizli Yereller bırakmak anlamına gelir  
  
 `ppProperty`  
 [out] Döndürür bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) yöntemi temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Gizli yerel öğeler, genellikle derleyici tarafından oluşturulan değişkenleri de kullanılabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugExpressionEvaluator](../../../extensibility/debugger/reference/idebugexpressionevaluator.md)   
 [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)   
 [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)   
 [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)

