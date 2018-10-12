---
title: dwTYPE_KIND | Microsoft Docs
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
- dwTYPE_KIND
helpviewer_keywords:
- dwTYPE_KIND enumeration
ms.assetid: 6ff56b0f-c502-4e6c-9829-bfa05361b783
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 8b77091d249de0c2f8c1171aa01707219f64f2b7
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49237802"
---
# <a name="dwtypekind"></a>dwTYPE_KIND
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Yorumlama türünü belirten bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) nesne.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
enum enum_dwTYPE_KIND {  
   TYPE_KIND_METADATA = 0x0001,  
   TYPE_KIND_PDB      = 0x0002,  
   TYPE_KIND_BUILT    = 0x0003,  
};  
  
typedef DWORD dwTYPE_KIND;  
```  
  
```csharp  
public enum enum_dwTYPE_KIND {  
   TYPE_KIND_METADATA = 0x0001,  
   TYPE_KIND_PDB      = 0x0002,  
   TYPE_KIND_BUILT    = 0x0003,  
};  
```  
  
#### <a name="parameters"></a>Parametreler  
 TYPE_KIND_METADATA  
 [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md) birleşim olarak yorumlanabilir bir [METADATA_TYPE](../../../extensibility/debugger/reference/metadata-type.md) yapısı.  
  
 TYPE_KIND_PDB  
 `TYPE_INFO` Birleşim olarak yorumlanabilir bir [PDB_TYPE](../../../extensibility/debugger/reference/pdb-type.md) yapısı.  
  
 TYPE_KIND_BUILT  
 `TYPE_INFO` Birleşim olarak yorumlanabilir bir [BUILT_TYPE](../../../extensibility/debugger/reference/built-type.md) yapısı.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu sabit listesi değerlerini görünür `dwKind` alanını [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md) yapısı ve nasıl yorumlanacağını belirlemek için kullanılan `type` birleşim üyesi. `TYPE_INFO` Yapısı için bir çağrı tarafından döndürülen [GetTypeInfo](../../../extensibility/debugger/reference/idebugfield-gettypeinfo.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)   
 [GetTypeInfo](../../../extensibility/debugger/reference/idebugfield-gettypeinfo.md)   
 [METADATA_TYPE](../../../extensibility/debugger/reference/metadata-type.md)   
 [PDB_TYPE](../../../extensibility/debugger/reference/pdb-type.md)   
 [BUILT_TYPE](../../../extensibility/debugger/reference/built-type.md)

