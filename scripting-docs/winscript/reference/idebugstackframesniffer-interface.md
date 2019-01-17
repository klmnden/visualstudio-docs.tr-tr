---
title: Idebugstackframesniffer arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugStackFrameSniffer interface
ms.assetid: 5669598e-a6bd-4694-9cb2-bd908be72bed
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 41fff384bc9075d94fcfa84d94350fec72ebc64a
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54348886"
---
# <a name="idebugstackframesniffer-interface"></a>IDebugStackFrameSniffer Arabirimi
Bir bileşen tarafından bilinen mantıksal yığın çerçevelerini numaralandırmak için bir yol sağlar. Komut dosyası motorları, genellikle bu arabirimi uygulayın. Bu arabirim tüm yığın çerçevelerini bulmak için işlemi hata ayıklama Yöneticisi kullanır, belirli bir iş parçacığı ile ilişkili.  
  
> [!NOTE]
>  Hata ayıklayıcı bu arabirimden ilgilendiğiniz iş parçacığı içinden çağırır. Komut dosyası altyapısı, geçerli iş parçacığını tanımlamak ve uygun bir numaralandırıcı döndürür.  
  
## <a name="methods"></a>Yöntemler  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IDebugStackFrameSniffer` arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugStackFrameSniffer::EnumStackFrames](../../winscript/reference/idebugstackframesniffer-enumstackframes.md)|Geçerli iş parçacığı için yığın çerçevelerinin bir numaralandırıcı döndürür.|