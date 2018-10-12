---
title: 'Nasıl yapılır: bir komut isteminden bir Profiler Karşılaştırma raporu oluşturma | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 00548d16-eb5b-46f7-8a65-862f98a43831
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2d3a36ac7a64c9e84b712bc0e7536f284375912c
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49258476"
---
# <a name="how-to-create-a-profiler-comparison-report-from-a-command-prompt"></a>Nasıl yapılır: Komut İsteminden Profil Oluşturucu Karşılaştırma Raporu Oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Oluşturabileceğiniz bir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] profil oluşturma araçları rapor iki profil oluşturma verilerinin performans verilerini karşılaştırır (. VSP ya. VSPS) dosyaları. Rapor farklar, performans gerilemeleri ve bir profil oluşturma oturumundan diğerine oluştu iyileştirmeleri gösterir. Rapordaki değerler delta veya belirttiğiniz ilk dosyanın temel bir değişiklik sunar. Bu delta temel değeri olan eski değer sonuç değeri arasındaki farkı yeni analiz belirleyerek hesaplanır. Profil Oluşturucu veri karşılaştırmalarını temel işlevler kodu, uygulama, çizgiler, yönerge işaretçileri (IP) ve türleri modüllerde alabilir.  
  
 Tanımlayıcıları karşılaştırma kategorileri ve alanların listesi için aşağıdaki komutu yazın:  
  
 **VSPerfReport/querydifftables***VspFileName1* *VspFileName2*  
  
 Karşılaştırma raporu oluşturmak için aşağıdaki sözdizimini kullanın:  
  
 **VSPerfReport/diff** `VspFileName1` *VspFileName2* [**/**`Options`]    
  
 Seçenekleri için aşağıdaki tablodan ekleyebileceğiniz **VSPerfReport/diff** komut satırı.  
  
|Seçenek|Açıklama|  
|------------|-----------------|  
|**DiffThreshold:**[*değer*]|Bu yüzdesi eşik değerinin altındaysa fark göz ardı edin. Ayrıca bu eşiğin altında olan değerlerle yeni bir veri görüntülenmez.|  
|**DiffTable:** *TableName*|Dosyayı karşılaştırmak için bu tabloyu kullanın. Varsayılan olarak, İşlevler tablosuna kullanılır. Listelenen tanımlayıcısını belirtin **VSPerfReport/querydifftables**.|  
|**DiffColumn:** *ColumnName*|Bu sütun değerleri karşılaştırmak için kullanın. Varsayılan olarak, özel örnekler Yüzde sütunu kullanılır. Listelenen tanımlayıcısını belirtin **VSPerfReport/querydifftables**.|



