---
title: IEnumDebugFields | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IEnumDebugFields
helpviewer_keywords:
- IEnumDebugFields interface
ms.assetid: 403c2a51-3ba5-431f-a1dd-2f3b2046c00c
caps.latest.revision: 7
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 5e3c9a43b6903522fe2caf0e329f8e8faa69cd6b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54792439"
---
# <a name="ienumdebugfields"></a>IEnumDebugFields
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu arabirimi uygulayan nesnelerin bir koleksiyonunu temsil eder [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) arabirimi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IEnumDebugFields : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bu arabirimi uygulayan nesne kümeleri sağlamak için Sembol sağlayıcısı tarafından uygulanan [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) arabirimi. Bu varlığı nedeniyle standart bir COM numaralandırma olmadığını unutmayın [GetCount](../../../extensibility/debugger/reference/ienumdebugfields-getcount.md) yöntemi.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Bu arabirim tarafından döndürülen [GetMethodFieldsByName](../../../extensibility/debugger/reference/idebugsymbolprovider-getmethodfieldsbyname.md) ve [GetNamespacesUsedAtAddress](../../../extensibility/debugger/reference/idebugsymbolprovider-getnamespacesusedataddress.md).  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Bu arabirim, aşağıdaki yöntemleri uygular.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[Next](../../../extensibility/debugger/reference/ienumdebugfields-next.md)|Sonraki alır [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) nesnelerden sabit listesi.|  
|[Skip](../../../extensibility/debugger/reference/ienumdebugfields-skip.md)|Belirtilen bir girdi sayısı atlar.|  
|[Reset](../../../extensibility/debugger/reference/ienumdebugfields-reset.md)|Numaralandırma ilk girişe sıfırlar.|  
|[Clone](../../../extensibility/debugger/reference/ienumdebugfields-clone.md)|Geçerli sabit bir kopyasını alır.|  
|[GetCount](../../../extensibility/debugger/reference/ienumdebugfields-getcount.md)|Sabit listesi içerisindeki giriş sayısını alır.|  
  
## <a name="remarks"></a>Açıklamalar  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sembol sağlayıcısı arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)   
 [GetMethodFieldsByName](../../../extensibility/debugger/reference/idebugsymbolprovider-getmethodfieldsbyname.md)   
 [GetNamespacesUsedAtAddress](../../../extensibility/debugger/reference/idebugsymbolprovider-getnamespacesusedataddress.md)
