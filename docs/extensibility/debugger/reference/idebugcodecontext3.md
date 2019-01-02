---
title: IDebugCodeContext3 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDebugCodeContext3 interface
ms.assetid: 524eb882-0ad5-4bfb-95eb-eb3abb3d0237
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: c4632e2a616bbc5c93cd6fb6ed2375217d4fd2b6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53927408"
---
# <a name="idebugcodecontext3"></a>IDebugCodeContext3
Genişletir [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) modülü ve işlem arabirimleri alınmasını etkinleştirmek için arabirim.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugCodeContext3 : IDebugCodeContext2  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Hata ayıklama motoru tarafından uygulanan ve tarafından tüketilen [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] paketinin hatalarını ayıkla.  
  
## <a name="methods"></a>Yöntemler  
 Yöntemlere ek olarak `IDebugCodeContext2` arabirimi bu arabirim, aşağıdaki yöntemleri uygular:  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[GetModule](../../../extensibility/debugger/reference/idebugcodecontext3-getmodule.md)|Hata ayıklama modülü arabirimine bir başvuru alır.|  
|[GetProcess](../../../extensibility/debugger/reference/idebugcodecontext3-getprocess.md)|Hata ayıklama işlemini arabirimine bir başvuru alır.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu genellikle uygulanacak bulunmayan isteğe bağlı bir arabirimdir.  
  
## <a name="requirements"></a>Gereksinimler  
 Üst bilgi: Msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll