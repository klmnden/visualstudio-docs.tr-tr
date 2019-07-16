---
title: DEBUG_PROPERTY_INFO | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- DEBUG_PROPERTY_INFO
helpviewer_keywords:
- DEBUG_PROPERTY_INFO structure
ms.assetid: 5a085d18-62c6-4740-b9e9-3f5db6bfdf7f
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 4c4200cb5a44e185d50158829fe44152707ee459
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68143040"
---
# <a name="debugpropertyinfo"></a>DEBUG_PROPERTY_INFO
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Hata ayıklama özelliği hakkında bilgiler içerir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
typedef struct tagDEBUG_PROPERTY_INFO {   
   DEBUGPROP_INFO_FLAGS dwValidFields;  
   BSTR                 bstrFullName;  
   BSTR                 bstrName;  
   BSTR                 bstrType;  
   BSTR                 bstrValue;  
   IDebugProperty2*     pProperty;  
   DBG_ATTRIB_FLAGS     dwAttrib;  
} DEBUG_PROPERTY_INFO;  
```  
  
```csharp  
public struct DEBUG_PROPERTY_INFO {   
   public uint            dwValidFields;  
   public string          bstrFullName;  
   public string          bstrName;  
   public string          bstrType;  
   public string          bstrValue;  
   public IDebugProperty2 pProperty;  
   public ulong           dwAttrib;  
};  
```  
  
## <a name="members"></a>Üyeler  
 dwValidFields  
 Bayraklarının bir birleşimi [DEBUGPROP_INFO_FLAGS](../../../extensibility/debugger/reference/debugprop-info-flags.md) hangi alanların doldurulur belirten sabit listesi.  
  
 bstrFullName  
 Özelliğin tam adı.  
  
 bstrName  
 Bir bağlam içinde özellik adı.  
  
 bstrType  
 Özellik türü olarak biçimlendirilmiş bir dize.  
  
 bstrValue  
 Özellik değeri olarak biçimlendirilmiş bir dize.  
  
 pProperty  
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) bu yapı tarafından açıklanan bir nesne.  
  
 dwAttrib  
 Bayraklarının bir birleşimi [DBG_ATTRIB_FLAGS](../../../extensibility/debugger/reference/dbg-attrib-flags.md) bu özelliğin özniteliklerini açıklayan sabit listesi.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir özellik adı, türü ve değeri içeren hiyerarşik bir yapısı nesnesidir. Örneğin, bir özellik, yerel değişkenler, parametreleri, izleme değişkenleri ve ifadeleri ve kayıtları açıklayabilirsiniz.  
  
 Bu yapı geçirilir [GetPropertyInfo](../../../extensibility/debugger/reference/idebugproperty2-getpropertyinfo.md) yöntemi burada da doldurulur. Bu yapı ayrıca bir liste bu yapının bir parçası olarak döndürülen [IEnumDebugPropertyInfo2](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2.md) hangi sırayla çağrısından döndürülen arabirimi [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md) ve [ EnumProperties](../../../extensibility/debugger/reference/idebugstackframe2-enumproperties.md) yöntemleri.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yapılar ve birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [DEBUGPROP_INFO_FLAGS](../../../extensibility/debugger/reference/debugprop-info-flags.md)   
 [DBG_ATTRIB_FLAGS](../../../extensibility/debugger/reference/dbg-attrib-flags.md)   
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)   
 [GetPropertyInfo](../../../extensibility/debugger/reference/idebugproperty2-getpropertyinfo.md)   
 [IEnumDebugPropertyInfo2](../../../extensibility/debugger/reference/ienumdebugpropertyinfo2.md)   
 [EnumChildren](../../../extensibility/debugger/reference/idebugproperty2-enumchildren.md)   
 [EnumProperties](../../../extensibility/debugger/reference/idebugstackframe2-enumproperties.md)
