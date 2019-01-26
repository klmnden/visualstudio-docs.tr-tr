---
title: METADATA_TYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- METADATA_TYPE
helpviewer_keywords:
- METADATA_TYPE structure
ms.assetid: 2d8b78f6-0aef-4d79-809a-cff9b2c24659
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8c276c34b902358ab355f1a67ffa1d97f4f0f8ce
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55034723"
---
# <a name="metadatatype"></a>METADATA_TYPE
Bu yapı meta verilerinden harcanan alan türü hakkında bilgileri belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
typedef struct _tagTYPE_METADATA {  
   ULONG32  ulAppDomainID;  
   GUID     guidModule;  
   _mdToken tokClass;  
} METADATA_TYPE;  
```  
  
```csharp  
public struct METADATA_TYPE {  
   public uint ulAppDomainID;  
   public Guid guidModule;  
   public int  tokClass;  
};  
```  
  
#### <a name="parameters"></a>Parametreler  
 ulAppDomainID  
 Simgenin içinden gelen uygulama kimliği. Bu, uygulamanın bir örneğini benzersiz şekilde tanımlamak için kullanılır.  
  
 guidModule  
 Bu alan içeren modül GUID.  
  
 tokClass  
 Bu tür meta veri belirteci kimliği.  
  
 [C++] `_mdToken` olduğu bir `typedef` 32-bit `int`.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yapı birleşimde bir parçası olarak görünür [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md) ne zaman yapısı `dwKind` alanını `TYPE_INFO` yapısı ayarlandığında `TYPE_KIND_METADATA` (arasında bir değer [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md) sabit listesi).  
  
 `tokClass` Türü benzersiz olarak tanımlayan bir meta veri belirteci değerdir. Meta veri belirteci kimliği üst bitlerini yorumlama hakkında ayrıntılı bilgi için bkz. `CorTokenType` numaralandırma corhdr.h dosyasında [!INCLUDE[dnprdnshort](../../../code-quality/includes/dnprdnshort_md.md)] SDK.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yapılar ve birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)   
 [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md)