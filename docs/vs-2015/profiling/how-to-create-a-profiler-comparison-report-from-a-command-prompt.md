---
title: 'Nasıl yapılır: Bir komut isteminden bir Profiler Karşılaştırma raporu oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 00548d16-eb5b-46f7-8a65-862f98a43831
caps.latest.revision: 15
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 8c6dabbae5f2d3758aebe0562f99767ee6993d80
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54756745"
---
# <a name="how-to-create-a-profiler-comparison-report-from-a-command-prompt"></a>Nasıl yapılır: Bir komut isteminden bir Profiler Karşılaştırma raporu oluşturma
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
