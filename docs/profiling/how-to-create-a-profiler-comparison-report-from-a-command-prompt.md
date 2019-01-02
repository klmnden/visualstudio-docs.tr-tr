---
title: 'Nasıl Yapılır: Bir komut isteminden bir Profiler Karşılaştırma raporu oluşturma | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 00548d16-eb5b-46f7-8a65-862f98a43831
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e63e366bbfe29d56ffc61085e986372ac0a9a2f5
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53880773"
---
# <a name="how-to-create-a-profiler-comparison-report-from-a-command-prompt"></a>Nasıl Yapılır: Komut isteminden profil oluşturucu karşılaştırma raporu oluşturma
Oluşturabileceğiniz bir [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma araçları rapor iki profil oluşturma verilerinin performans verilerini karşılaştırır (. *Vsp* ya. *vsps*) dosyaları. Rapor farklar, performans gerilemeleri ve bir profil oluşturma oturumundan diğerine oluştu iyileştirmeleri gösterir. Rapordaki değerler delta veya belirttiğiniz ilk dosyanın temel bir değişiklik sunar. Bu delta temel değeri olan eski değer sonuç değeri arasındaki farkı yeni analiz belirleyerek hesaplanır. Profil Oluşturucu veri karşılaştırmalarını temel işlevler kodu, uygulama, çizgiler, yönerge işaretçileri (IP) ve türleri modüllerde alabilir.  
  
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