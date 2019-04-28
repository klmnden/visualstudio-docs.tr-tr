---
title: Idebugstackframesniffer arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 5c9181b5013a9584a2a686ed0e499698be0b62b9
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63432264"
---
# <a name="idebugstackframesniffer-interface"></a>IDebugStackFrameSniffer Arabirimi
Bir bileşen tarafından bilinen mantıksal yığın çerçevelerini numaralandırmak için bir yol sağlar. Komut dosyası motorları, genellikle bu arabirimi uygulayın. Bu arabirim tüm yığın çerçevelerini bulmak için işlemi hata ayıklama Yöneticisi kullanır, belirli bir iş parçacığı ile ilişkili.  
  
> [!NOTE]
> Hata ayıklayıcı bu arabirimden ilgilendiğiniz iş parçacığı içinden çağırır. Komut dosyası altyapısı, geçerli iş parçacığını tanımlamak ve uygun bir numaralandırıcı döndürür.  
  
## <a name="methods"></a>Yöntemler  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IDebugStackFrameSniffer` arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugStackFrameSniffer::EnumStackFrames](../../winscript/reference/idebugstackframesniffer-enumstackframes.md)|Geçerli iş parçacığı için yığın çerçevelerinin bir numaralandırıcı döndürür.|