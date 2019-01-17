---
title: Idebugstackframesnifferex arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugStackFrameSnifferEx interface
ms.assetid: fd6cf744-dee7-45f2-9a90-355b90372923
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 76f10d6bbb34c61e87a1be0f61dcd7db168274e7
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54348496"
---
# <a name="idebugstackframesnifferex-interface"></a>IDebugStackFrameSnifferEx Arabirimi
Bir bileşen tarafından bilinen mantıksal yığın çerçevelerini numaralandırmak için bir yol sağlar. Komut dosyası motorları, genellikle bu arabirimi uygulayın. Bu arabirim tüm yığın çerçevelerini bulmak için işlemi hata ayıklama Yöneticisi kullanır, belirli bir iş parçacığı ile ilişkili.  
  
> [!NOTE]
>  Bu arabirim ilgilendiğiniz iş parçacığı içinde çağrılır. Arabirimi uygulama, geçerli iş parçacığını tanımlamak ve uygun bir numaralandırıcı döndürür.  
  
 Devralınan yöntemleri yanı sıra `IDebugStackFrameSniffer`, `IDebugStackFrameSnifferEx` arabirimi aşağıdaki yöntemleri sunar.  
  
## <a name="methods-in-vtable-order"></a>Vtable sırayla yöntemleri  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugStackFrameSnifferEx::EnumStackFramesEx](../../winscript/reference/idebugstackframesnifferex-enumstackframesex.md)|Geçerli iş parçacığı için yığın çerçevelerinin bir numaralandırıcı döndürür.|