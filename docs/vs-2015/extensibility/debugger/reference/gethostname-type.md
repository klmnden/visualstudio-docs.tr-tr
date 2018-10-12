---
title: GETHOSTNAME_TYPE | Microsoft Docs
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
- GETHOSTNAME_TYPE
helpviewer_keywords:
- GETHOSTNAME_TYPE enumeration
ms.assetid: 2be92bea-8133-412b-9015-1833baf16e1b
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1235592e9da0f677867cb1b882a935f30cdc5c2f
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49299732"
---
# <a name="gethostnametype"></a>GETHOSTNAME_TYPE
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Ana bilgisayar adı türünü belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
enum enum_GETHOSTNAME_TYPE {   
   GHN_FRIENDLY_NAME = 0,  
   GHN_FILE_NAME     = 1  
};  
typedef DWORD GETHOSTNAME_TYPE;  
```  
  
```csharp  
public enum enum_GETHOSTNAME_TYPE {   
   GHN_FRIENDLY_NAME = 0,  
   GHN_FILE_NAME     = 1  
};  
```  
  
## <a name="members"></a>Üyeler  
 GHN_FRIENDLY_NAME  
 Ana bilgisayarın kolay bir ad belirtir.  
  
 GHN_FILE_NAME  
 Ana bilgisayar dosya adını belirtir.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu değerleri bir bağımsız değişken olarak geçirilen [GetHostName](../../../extensibility/debugger/reference/idebugprogramnode2-gethostname.md) farklı biçimlerde bir ana bilgisayar adı almak için yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetHostName](../../../extensibility/debugger/reference/idebugprogramnode2-gethostname.md)

