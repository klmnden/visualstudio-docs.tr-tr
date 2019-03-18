---
title: Idebugstackframesnifferex arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: dc6e892c00a2d86e784857f08772550897e1ec4e
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58157192"
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