---
title: IDebugStopCompleteEvent2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- IDebugStopCompleteEvent2 interface
ms.assetid: ff3e89f4-61bb-489d-901c-447260100218
caps.latest.revision: 7
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: a9c2a6a6e69bf47751706710801dd78c832ccd2c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62546929"
---
# <a name="idebugstopcompleteevent2"></a>IDebugStopCompleteEvent2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir program durduğunda, hata ayıklama altyapısı (DE) oturum hata ayıklama Yöneticisi (SDM) Bu isteğe bağlı bir olay gönderebilirsiniz.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
IDebugStopCompleteEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Uygulayanlar için Notlar  
 Yeni bir arabirimi budur [!INCLUDE[vsprvslong](../../../includes/vsprvslong-md.md)]. Önceki sürümlerde, zaman uyumsuz durdurma desteklememektedir.  
  
 [Durdur](../../../extensibility/debugger/reference/idebugengineprogram2-stop.md) SDM senaryolarda, çok işlemli veya çok programı tarafından çağrılır. Bir program için SDM durdurma olay gönderdiğinde SDM çok durdurmak için diğer programları ister.  
  
 Zaman uyumsuz olarak bir program durduktan SDM bildirmek için kullanılır. Bazen kod hata ayıklaması yapılan programa içinde çalıştığı, yorumlayıcı hata ayıklama altyapısı için kullanışlıdır şekilde [Durdur](../../../extensibility/debugger/reference/idebugengineprogram2-stop.md) zaman uyumlu olarak tamamlanamadı. Hata ayıklama altyapısı bu zaman uyumsuz bildirim görevlendirmek isteyip istemediği, döndürmesi gereken `S_ASYNC_STOP` gelen [Durdur](../../../extensibility/debugger/reference/idebugengineprogram2-stop.md).  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll
