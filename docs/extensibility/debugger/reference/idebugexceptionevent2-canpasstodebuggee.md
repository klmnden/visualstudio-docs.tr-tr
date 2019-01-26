---
title: IDebugExceptionEvent2::CanPassToDebuggee | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugExceptionEvent2::CanPassToDebuggee
helpviewer_keywords:
- IDebugExceptionEvent2::CanPassToDebuggee
ms.assetid: ae4bbe0a-fbe1-49be-a310-ea64279a434b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8ccf980fb3d5b357b6211674ca8b99132d81fae1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55041015"
---
# <a name="idebugexceptionevent2canpasstodebuggee"></a>IDebugExceptionEvent2::CanPassToDebuggee
Hata ayıklama altyapısı (DE) yürütme devam ettiğinde ayıklanan programa bu özel durum geçirme seçeneğiniz destekleyip desteklemediğini belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT CanPassToDebuggee(  
   void  
);  
```  
  
```csharp  
int CanPassToDebuggee();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` (özel durum programa geçirilebilir) veya `S_FALSE` (özel durum geçirilemez).  
  
## <a name="remarks"></a>Açıklamalar  
 Hata ayıklanan iletilecek bir varsayılan eylem DE olması gerekir. IDE alabilirsiniz [IDebugExceptionEvent2](../../../extensibility/debugger/reference/idebugexceptionevent2.md) olay ve arama [devam](../../../extensibility/debugger/reference/idebugprocess3-continue.md) yöntemi çağırmadan `CanPassToDebuggee` yöntemi. Bu nedenle DE özel durum veya geçirmek için bir varsayılan durumda olması gerekir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugExceptionEvent2](../../../extensibility/debugger/reference/idebugexceptionevent2.md)   
 [Continue](../../../extensibility/debugger/reference/idebugprocess3-continue.md)