---
title: Windows (ETW) raporu için olay izleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Event tracing for Windows profiling report
- ETW profiling report
ms.assetid: 81e88162-b88a-40b6-8b85-a232c8096a47
caps.latest.revision: 17
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: ba40e16f70451a288a17c138bdfa3b2070d56122
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54752255"
---
# <a name="event-tracing-for-windows-etw-report"></a>Windows için Olay İzleme (ETW) Raporu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir performans oturumu içinde kaydedilen ETW olayları için olay izleme Windows (ETW) raporu listeler [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] profil oluşturma araçları. ETW verilerini bir ikili (.etl) dosyasında toplanır.  
  
> [!NOTE]
>  ETW raporları görüntüleyemez [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] arabirimi.  
  
-   ETW profil oluşturma araçları kullanarak toplama hakkında bilgi için [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] arabirim için bkz: [nasıl yapılır: Olay izleme için Windows (ETW) verilerini toplama](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md).  
  
-   Kullanarak ETW veri toplama hakkında bilgi için [VSPerfCmd](../profiling/vsperfcmd.md) komut satırı araçları görmek [olayları](../profiling/events-vsperfcmd.md).  
  
-   Kullanarak ETW raporu oluşturma **VSReport / Summary: ETW** komutu. Daha fazla bilgi için [VSPerfReport](../profiling/vsperfreport.md).  
  
|Sütun|Açıklama|  
|------------|-----------------|  
|**Zaman damgası**|Olay gerçekleştiğinde tanımlar.|  
|**İşlem kimliği**|Olayı oluşturan bir işlemi tanımlar.|  
|**İş parçacığı kimliği**|Olayı oluşturan iş parçacığını tanımlar.|  
|**Açıklama**|Olay sağlayıcısı tanımlar.|  
|**Tür**|Olay türü tanımlar.|  
|**Özellikler**|Olay Özellikleri. Her olay, parantez içine alınmış bir virgülle ayrılmış, ad-değer çiftidir.|
