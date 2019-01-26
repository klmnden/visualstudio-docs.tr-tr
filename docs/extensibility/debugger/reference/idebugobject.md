---
title: IDebugObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugObject
helpviewer_keywords:
- IDebugObject interface
ms.assetid: 05cd8bf4-c9ee-4b49-b782-2263c33067d6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6b29382a7a4a75ecb6292e6d239657b23257dea0
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54941959"
---
# <a name="idebugobject"></a>IDebugObject
> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Bu arabirim, semboller ve ifadeleri değerlerini yalıtılacak Bağlayıcısı oluşturur. bir nesneyi temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugObject : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 İfade değerlendiricisi, bir nesneyi göstermek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 İfade değerlendirici ayrıştırılmış ifadeler kullanan tüm nesneleri için taban sınıf arabirimidir. Bir çağrı tarafından döndürülen [bağlama](../../../extensibility/debugger/reference/idebugbinder-bind.md) yöntemi. [QueryInterface](/cpp/atl/queryinterface) daha özel arabirimler bu arabirimden alır.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugObject`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetSize](../../../extensibility/debugger/reference/idebugobject-getsize.md)|Nesnenin boyutunu alır.|  
|[GetValue](../../../extensibility/debugger/reference/idebugobject-getvalue.md)|Nesnenin değerini ardışık bir bayt dizisi olarak alır.|  
|[SetValue](../../../extensibility/debugger/reference/idebugobject-setvalue.md)|Nesnenin değerini ardışık bir bayt serisinden ayarlar.|  
|[SetReferenceValue](../../../extensibility/debugger/reference/idebugobject-setreferencevalue.md)|Bu nesne başvuru değeri ayarlar.|  
|[GetMemoryContext](../../../extensibility/debugger/reference/idebugobject-getmemorycontext.md)|Nesne değeri adresini temsil eden bellek bağlamını alır.|  
|[GetManagedDebugObject](../../../extensibility/debugger/reference/idebugobject-getmanageddebugobject.md)|Hata ayıklama altyapısı adres alanında yönetilen nesnesinin bir kopyasını oluşturur.|  
|[IsNullReference](../../../extensibility/debugger/reference/idebugobject-isnullreference.md)|Bu nesne bir null başvuru olup olmadığını sınar.|  
|[IsEqual](../../../extensibility/debugger/reference/idebugobject-isequal.md)|Bu bir nesneyi karşılaştırır.|  
|[IsReadOnly](../../../extensibility/debugger/reference/idebugobject-isreadonly.md)|Bu nesne, salt okunur olup olmadığını belirler.|  
|[IsProxy](../../../extensibility/debugger/reference/idebugobject-isproxy.md)|Nesnenin saydam bir ara sunucu olup olmadığını belirler.|  
  
## <a name="remarks"></a>Açıklamalar  
 İfade değerlendirici bu arabirim, ayrıştırma ağacı nesneleri temsil etmek için temel sınıf olarak kullanır.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: ee.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İfade değerlendirme arabirimleri](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)   
 [GetElement](../../../extensibility/debugger/reference/idebugarrayobject-getelement.md)   
 [Bind](../../../extensibility/debugger/reference/idebugbinder-bind.md)