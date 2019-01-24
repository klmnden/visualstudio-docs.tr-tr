---
title: PDB_TYPE | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- PDB_TYPE
helpviewer_keywords:
- PDB_TYPE structure
ms.assetid: 1c1bb772-77d6-4870-90b2-fd9247d0004e
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: ad4b6a06a2a145daa85d780f4d23dfac9bebf7a0
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54801128"
---
# <a name="pdbtype"></a>PDB_TYPE
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yapı, PDB sembol harcanan alan türü hakkında bilgileri belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
typedef struct _tagTYPE_PDB {  
   ULONG32 ulAppDomainID;  
   GUID    guidModule;  
   DWORD   symid;  
} PDB_TYPE;  
```  
  
```csharp  
public struct PDB_TYPE {  
   public uint ulAppDomainID;  
   public Guid guidModule;  
   public uint symid;  
};  
```  
  
#### <a name="parameters"></a>Parametreler  
 ulAppDomainID  
 Simgenin içinden gelen uygulama kimliği. Bu, uygulamanın bir örneğini benzersiz şekilde tanımlamak için kullanılır.  
  
 guidModule  
 Bu alan içeren modül GUID.  
  
 symid  
 Bu alana karşılık gelen simgesinin kimliği.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yapı birleşimde bir parçası olarak görünür [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md) ne zaman yapısı `dwKind` alanını `TYPE_INFO` yapısı ayarlandığında `TYPE_KIND_PDB` (arasında bir değer [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md) sabit listesi).  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yapılar ve birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)   
 [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md)
