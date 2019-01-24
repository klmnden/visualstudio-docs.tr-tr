---
title: IDebugExceptionEvent2::CanPassToDebuggee | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugExceptionEvent2::CanPassToDebuggee
helpviewer_keywords:
- IDebugExceptionEvent2::CanPassToDebuggee
ms.assetid: ae4bbe0a-fbe1-49be-a310-ea64279a434b
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 383287a027a75adfb4c58020675e08a46198eacf
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54798489"
---
# <a name="idebugexceptionevent2canpasstodebuggee"></a>IDebugExceptionEvent2::CanPassToDebuggee
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Hata ayıklama altyapısı (DE) yürütme devam ettiğinde ayıklanan programa bu özel durum geçirme seçeneğiniz destekleyip desteklemediğini belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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
