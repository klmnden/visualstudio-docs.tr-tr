---
title: IDebugProgramDestroyEventFlags2 | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- IDebugProgramDestroyEventFlags2 interface
ms.assetid: d384ff71-dc71-40b9-a871-801f8b6a3418
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 9afc8a810468733661abb2a71e609e3cbe303d51
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49223619"
---
# <a name="idebugprogramdestroyeventflags2"></a>IDebugProgramDestroyEventFlags2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Varsayılan davranışı geçersiz kılmak bir hata ayıklama altyapısı sağlayan [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)] hata ayıklama oturumunu sonlandırdığınızda, kullanıcı Arabirimi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugProgramDestroyEventFlags2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Bu arabirim, hata ayıklama motoru tarafından uygulanır. Oluşturma ve bir işlem yaşam süresi boyunca birden çok program yok konaklar için kullanışlıdır.  
  
## <a name="methods"></a>Yöntemler  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir `IDebugProgramDestroyEventFlags2`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetFlags](../../../extensibility/debugger/reference/idebugprogramdestroyeventflags2-getflags.md)|Program alır bayrakları yok.|  
  
## <a name="remarks"></a>Açıklamalar  
 Varsayılan davranışını [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)] UI olan tüm programları bir program gönderdikten sonra Tasarım moduna geri dönmek için olay yok. Bu arabirim, bu davranışı değiştirmek bir hata ayıklama altyapısı sağlar.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

