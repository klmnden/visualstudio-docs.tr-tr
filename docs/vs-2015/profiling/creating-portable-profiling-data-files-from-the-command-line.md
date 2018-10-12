---
title: Profil oluşturma veri dosyaları komut satırından taşınabilir oluşturma | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 2ceb63a7-b835-4988-b756-2afc3fcc4808
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 8f2a2979fdc836f0204dec580d49e86ae235d5c1
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49254702"
---
# <a name="creating-portable-profiling-data-files-from-the-command-line"></a>Komut Satırından Taşınabilir Profil Oluşturma Veri Dosyaları Oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Profil oluşturma verilerini daha kolay paylaşım yapmak için kullanabileceğiniz [VSPerfReport](../profiling/vsperfreport.md) bir .vsp dosyasına profil oluşturma için simgeleri eklemek için komut satırı aracı.  
  
 Daha küçüktür ve IDE'de yük daha hızlı bir şekilde önceden çözümlenmiş bir profil oluşturma veri (.vsps) dosyası da oluşturabilirsiniz.  
  
> [!NOTE]
>  Sembol (.pdb) dosyalarının kullanılabilir olduğundan emin olun **VSPerfReport**. Daha fazla bilgi için [nasıl yapılır: komut satırından sembol dosyası konumu belirtin](../profiling/how-to-specify-symbol-file-locations-from-the-command-line.md).  
>   
>  Yolu hakkında bilgi için **VSReport**, bkz: [komut satırı araçları yolunu belirtme](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).  
>   
>  Profil oluşturma verilerinin bir .vsps dosyasında filtrelenemez.  
  
### <a name="to-embed-the-symbols-for-a-profiling-run-into-a-profiling-data-vsp-file"></a>Bir profil oluşturma veri (.vsp) dosyasına bir profil oluşturma için simgeleri eklemek için  
  
-   Bir komut istemi penceresinde, aşağıdaki komutu yazın:  
  
     \<Yolu >**VSPerfReport \<** VSP dosyası > **packsymbols**  
  
     Varsayılan olarak, .vsp dosyasının temel adı ile .vsps dosyası olarak adlandırılır. Kullanarak bir diğer ad belirtebilirsiniz **çıkış** seçeneği.  
  
### <a name="to-create-a-summary-profiling-data-file"></a>Özet bir profil oluşturma veri dosyasını oluşturmak için  
  
-   Bir komut istemi penceresinde, aşağıdaki komutu yazın:  
  
     \<Yolu >**VSPerfReport \<** VSP dosyası > **/summaryfile** [**/Output:**\<dosya adı >]  
  
     Varsayılan olarak, .vsp dosyasının temel adı ile .vsps dosyası olarak adlandırılır. Kullanarak bir diğer ad belirtebilirsiniz **çıkış** seçeneği.



