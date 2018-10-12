---
title: 'Nasıl yapılır: komut satırından raporları filtreleme | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 6e9b140f-b44f-4a5c-bd65-d868ddc94023
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5a93e1bb2e1d3a65d82a4a0ac54e903ee20553d4
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49290153"
---
# <a name="how-to-filter-reports-from-the-command-line"></a>Nasıl yapılır: Komut Satırından Raporları Filtreleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Seçeneklerini kullanarak **VSPerfReport** komutu, profil oluşturma veri dosyasının belirli bir zaman segmente raporları filtreleme veya bir veya daha fazla işlemlere veya iş parçacıklarına için veri kısıtlama. Bu komut hakkında daha fazla bilgi için bkz. [VSPerfReport](../profiling/vsperfreport.md).  
  
|Seçenekler|Açıklama|  
|-------------|-----------------|  
|**StartTime:**[*değer*]|Yalnızca (milisaniye cinsinden.) değerden sonra toplanan verileri göster|  
|**EndTime:**[*değer*]|Yalnızca (milisaniye cinsinden.) değerden önce toplanan verileri göster|  
|**FilterFile:** `VSPFFile`|Öğesinden oluşturulan bir filtre dosyasının konumunu belirtir **Visual Studio performans raporu** penceresi.|  
|**MsFilter:**[*StartTime, süre*]|Yalnızca verileri göstermek `StartTime` uzunluğuna kadar `Duration` (milisaniye cinsinden.)|  
|**İşlem:**[*PID*]|Yalnızca belirtilen işlemden verileri göster.|  
|**İş parçacığı:**[*ThreadID*]|Yalnızca belirtilen iş parçacığından verileri göster.|  
|**İş parçacığı:**[*ThreadID, ProcessId*]|Yalnızca belirtilen işlemle ilişkili belirtilen iş parçacığından verileri göster.|



