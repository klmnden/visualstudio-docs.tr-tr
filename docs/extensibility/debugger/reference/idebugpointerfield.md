---
title: IDebugPointerField | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPointerField
helpviewer_keywords:
- IDebugPointerField interface
ms.assetid: d51bd5b2-f18e-4e27-b4fb-e6f652fbf635
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 7fc686af78b4ac787abef1c0c52309e82c47376b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53947900"
---
# <a name="idebugpointerfield"></a>IDebugPointerField
Bu arabirim, bir işaretçi türü temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugPointerField : IDebugContainerField  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Sembol sağlayıcısı, bir işaretçiyi temsil etmek için bu arabirimi uygular.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Kullanım [QueryInterface](/cpp/atl/queryinterface) bu arabirimden edinme [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) , arabirim [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) döndürür `FIELD_TYPE_POINTER`.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Yöntemlere ek olarak `IDebugField` ve `IDebugContainerField` arabirimleri, bu arabirimi uygulayan aşağıdaki yöntemi:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetDereferencedField](../../../extensibility/debugger/reference/idebugpointerfield-getdereferencedfield.md)|Döndürür bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) işaretçinin hedef açıklayan.|  
  
## <a name="remarks"></a>Açıklamalar  
 C/C++'da bir işaretçi, dizi gösterim kullanılırsa, bir kapsayıcı olabilir. Örneğin, verilen `char *pString`, `pString` işaretçi türünde `char`. `pString[3]` bir işaretçi bir kapsayıcı türü olan `char` , bu kapsayıcı, dördüncü öğesine başvuruyor.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sembol sağlayıcısı arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)   
 [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md)