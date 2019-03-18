---
title: IDebugApplicationNode100::SetFilterForEventSink | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplicationNode100::SetFilterForEventSink
ms.assetid: cfb34efe-c6e1-4692-8ffd-3ede3a24cd4b
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f1a59f57daad90e5a7df1a8d8fa8d1ecd8c5c3bf
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58154302"
---
# <a name="idebugapplicationnode100setfilterforeventsink"></a>IDebugApplicationNode100::SetFilterForEventSink
Belirli bir filtre ayarlar [Idebugapplicationnodeevents arabirimi](../../winscript/reference/idebugapplicationnodeevents-interface.md) uygulaması. PDM artık oluşturduğunuz veya kaldırıldığında bu olayları gönderir, böylece alt derleyici tarafından oluşturulan uygulama düğümlerini filtrelemek betik hata ayıklayıcıları sağlar. Varsayılan olarak tüm düğümleri gönderilir.  
  
> [!IMPORTANT]
>  [Idebugapplicationnode100 arabirimi](../../winscript/reference/idebugapplicationnode100-interface.md) PDM v10.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT SetFilterForEventSink(        [in] DWORD dwCookie,        [in] APPLICATION_NODE_EVENT_FILTER filter        );  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwCookie`  
 Filtrenin tanımlama bilgisi.  
  
 `filter`  
 Filtre.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplicationNode100 Arabirimi](../../winscript/reference/idebugapplicationnode100-interface.md)