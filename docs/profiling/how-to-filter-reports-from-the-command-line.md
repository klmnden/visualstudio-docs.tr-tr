---
title: 'Nasıl yapılır: Komut satırından raporları filtreleme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 6e9b140f-b44f-4a5c-bd65-d868ddc94023
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d55438c95bcb82306afde7c65c22f3f29b98578d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/26/2019
ms.locfileid: "55069232"
---
# <a name="how-to-filter-reports-from-the-command-line"></a>Nasıl yapılır: Komut satırından raporları filtreleme
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