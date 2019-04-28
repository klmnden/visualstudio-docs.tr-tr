---
title: Iremotedebugapplication110 arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IRemoteDebugApplication110 Interface
ms.assetid: 785ab46a-8827-41cb-806a-132e6b2c8f47
caps.latest.revision: 3
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ea8f3f983cf7279cf6dc9600813a08268cef8301
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63383488"
---
# <a name="iremotedebugapplication110-interface"></a>IRemoteDebugApplication110 Arabirimi
Betik hata ayıklayıcıları tarafından çağrılabilir ve işlem içi çağıranlar yeni özellikler sağlamak için kullanılır.  
  
> [!IMPORTANT]
> Bu arabirim PDM v11.0 ve sonraki sürümler tarafından uygulanır. activdbg100.h içinde bulunur.  
  
## <a name="methods"></a>Yöntemler  
 `IRemoteDebugApplication110` Arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IRemoteDebugApplication110::SetDebuggerOptions](../../winscript/reference/iremotedebugapplication110-setdebuggeroptions.md)|Hata ayıklayıcısı Seçenekleri güncelleştirmek için çağrıldı. Seçenekleri varsayılan olarak 0 (SDO_NONE).|  
|[IRemoteDebugApplication110::GetCurrentDebuggerOptions](../../winscript/reference/iremotedebugapplication110-getcurrentdebuggeroptions.md)|Geçerli etkin seçenekleri kümesi döndürür.|  
|[IRemoteDebugApplication110::GetMainThread](../../winscript/reference/iremotedebugapplication110-getmainthread.md)|Ana iş parçacığı SetSite çağıran ana bilgisayarlar için döndürür.|