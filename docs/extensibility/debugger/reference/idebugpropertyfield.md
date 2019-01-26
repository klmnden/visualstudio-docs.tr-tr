---
title: IDebugPropertyField | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPropertyField
helpviewer_keywords:
- IDebugPropertyField interface
ms.assetid: b50edb2c-fb8d-4def-993d-17d23d2027c1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 017ab4116654bb341162e46352dcb16b85528a74
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54995914"
---
# <a name="idebugpropertyfield"></a>IDebugPropertyField
Bu arabirim, alma ve bir özellik ayarlama izin işlevleri sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugPropertyField : IDebugContainerField  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Sembol sağlayıcısı bu arabirimi uygulayan aynı nesne üzerinde uygulayan [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md). Bu sınıfta özellikleri kavramını destekleyen bir özelleştirmesi arabirimidir.  
  
## <a name="notes-for-callers"></a>Arayanlar İçin Notlar  
 Kullanım [QueryInterface](/cpp/atl/queryinterface) bu arabirimden edinme [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md) , arabirim [GetKind](../../../extensibility/debugger/reference/idebugfield-getkind.md) yöntemi döndürür `FIELD_KIND_PROP`.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
 Yöntemlere ek olarak [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) ve [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md) arabirimleri, bu arabirimi aşağıdaki yöntemleri uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetPropertyGetter](../../../extensibility/debugger/reference/idebugpropertyfield-getpropertygetter.md)|Özelliği alır yöntemi alır.|  
|[GetPropertySetter](../../../extensibility/debugger/reference/idebugpropertyfield-getpropertysetter.md)|Özelliği ayarlar yönteminin alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir özellik, yönetilen kod kavram ve bir değişken olarak kabul edilir bir yöntemi temsil eder. Yönetilmeyen C++'da özellikleri yok.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sembol sağlayıcısı arabirimleri](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [IDebugContainerField](../../../extensibility/debugger/reference/idebugcontainerfield.md)