---
title: marker_series::marker_series Oluşturucusu | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- cvmarkersobj/Concurrency::diagnostic::marker_series::marker_series
helpviewer_keywords:
- Concurrency::diagnostic::marker_series constructor
ms.assetid: 042c7d23-f1d8-4e09-9e76-a21c30243790
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6dfd38ef661ad050d36c8a157186094bc5316caf
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49190833"
---
# <a name="markerseriesmarkerseries-constructor"></a>marker_series::marker_series Oluşturucusu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yeni bir örneğini başlatır `marker_series` sınıfı.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
marker_series();  
marker_series(  
   _In_ LPCTSTR _SeriesName  
);  
marker_series(  
   _In_ const GUID* _ProviderGuid  
);  
marker_series(  
   _In_ const GUID* _ProviderGuid,  
   _In_ LPCTSTR _SeriesName  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `_SeriesName`  
 Oluşturulacak dizinin adı.  
  
 `_ProviderGuid`  
 Seri sağlayıcısı GUID.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** cvmarkersobj.h  
  
 **Namespace:** Concurrency::diagnostic  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [marker_series Sınıfı](../profiling/marker-series-class.md)



