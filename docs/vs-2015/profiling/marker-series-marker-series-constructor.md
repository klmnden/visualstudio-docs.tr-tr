---
title: marker_series::marker_series Oluşturucusu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- cvmarkersobj/Concurrency::diagnostic::marker_series::marker_series
helpviewer_keywords:
- Concurrency::diagnostic::marker_series constructor
ms.assetid: 042c7d23-f1d8-4e09-9e76-a21c30243790
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: b42058e0501612acbf454df725a9f1631489d26e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54788309"
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
  
 **Namespace:** CONCURRENCY::Diagnostic  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [marker_series Sınıfı](../profiling/marker-series-class.md)
