---
title: Idebugapplicationnode100 arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplicationNode100 Interface
ms.assetid: 43966d4e-5f89-4a04-a08d-782347d00c2d
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4a6cbe92c6789b702adc69f598a995f84c01ef86
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54347461"
---
# <a name="idebugapplicationnode100-interface"></a>IDebugApplicationNode100 Arabirimi
`IDebugApplicationNode100` Arabirimi işlevselliğini genişleten [Idebugapplicationnode arabirimi](../../winscript/reference/idebugapplicationnode-interface.md). Uygulaması QueryInterface çağırarak bu arabirimin örneğini alabilirsiniz [Idebugapplicationnode arabirimi](../../winscript/reference/idebugapplicationnode-interface.md).  
  
> [!IMPORTANT]
>  Bu arabirim PDM v10.0 ve büyük uygulanır. activdbg100.h içinde bulunur.  
  
## <a name="methods"></a>Yöntemler  
 `IDebugApplicationNode100` Arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugApplicationNode100::GetExcludedDocuments](../../winscript/reference/idebugapplicationnode100-getexcludeddocuments.md)|Belirtilen filtre tarafından gizlenen metin belgeleri alır.|  
|[IDebugApplicationNode100::QueryIsChildNode](../../winscript/reference/idebugapplicationnode100-queryischildnode.md)|Belirtilen belge bu düğümün alt düğümleri birine ait olup olmadığını belirler.|  
|[IDebugApplicationNode100::SetFilterForEventSink](../../winscript/reference/idebugapplicationnode100-setfilterforeventsink.md)|Belirli bir filtre ayarlar [Idebugapplicationnodeevents arabirimi](../../winscript/reference/idebugapplicationnodeevents-interface.md) uygulaması. PDM artık düğümlerin oluşturulduğunda veya kaldırılan olayları gönderir, böylece alt derleyici tarafından oluşturulan uygulama düğümlerini filtrelemek betik hata ayıklayıcıları sağlar. Varsayılan olarak tüm düğümleri gönderilir.|