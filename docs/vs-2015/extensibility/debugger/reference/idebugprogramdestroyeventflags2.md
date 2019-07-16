---
title: IDebugProgramDestroyEventFlags2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- IDebugProgramDestroyEventFlags2 interface
ms.assetid: d384ff71-dc71-40b9-a871-801f8b6a3418
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 86f7e211c742e4d95f3459d058139854874e7d85
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68182206"
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
 Üst bilgi: Msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll
