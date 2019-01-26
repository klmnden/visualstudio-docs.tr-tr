---
title: IEnumDebugAddresses | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEnumDebugAddresses
helpviewer_keywords:
- IEnumDebugAddresses interface
ms.assetid: 5f6f6751-e6d8-4c5a-8e81-414b6e5d8cc5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0b4dc67d421928bb9c962650dcad4a1c385665a9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55027730"
---
# <a name="ienumdebugaddresses"></a>IEnumDebugAddresses
Bu arabirimi uygulayan nesnelerin bir koleksiyonunu temsil eder [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IEnumDebugAdresses : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bu arabirimi uygulayan nesne kümeleri sağlamak için Sembol sağlayıcısı tarafından uygulanan [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) arabirimi. Bu varlığı nedeniyle standart bir COM numaralandırma olmadığını unutmayın [GetCount](../../../extensibility/debugger/reference/ienumdebugaddresses-getcount.md) yöntemi.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirim tarafından döndürülen [GetAddressesFromContext](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromcontext.md) ve [GetAddressesFromPosition](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromposition.md).  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Bu arabirim, aşağıdaki yöntemleri uygular.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Next](../../../extensibility/debugger/reference/ienumdebugaddresses-next.md)|Sonraki alır [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md) nesnelerden sabit listesi.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugaddresses-skip.md)|Belirtilen bir girdi sayısı atlar.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugaddresses-reset.md)|Numaralandırma ilk girişe sıfırlar.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugaddresses-clone.md)|Geçerli sabit bir kopyasını alır.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugaddresses-getcount.md)|Sabit listesi içerisindeki giriş sayısını alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu arabirim, genellikle için ifade değerlendirici vermek için uygun adresi belirlemeye yardımcı olması için hata ayıklama altyapısı tarafından kullanılır.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sembol sağlayıcısı arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)   
 [GetAddressesFromContext](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromcontext.md)   
 [GetAddressesFromPosition](../../../extensibility/debugger/reference/idebugsymbolprovider-getaddressesfromposition.md)