---
title: Profil oluşturma veri dosyaları komut satırından taşınabilir oluşturma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 2ceb63a7-b835-4988-b756-2afc3fcc4808
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5d343392c9e554c5e51325964949cd3ea13237b8
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63434284"
---
# <a name="creating-portable-profiling-data-files-from-the-command-line"></a>Komut Satırından Taşınabilir Profil Oluşturma Veri Dosyaları Oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Profil oluşturma verilerini daha kolay paylaşım yapmak için kullanabileceğiniz [VSPerfReport](../profiling/vsperfreport.md) bir .vsp dosyasına profil oluşturma için simgeleri eklemek için komut satırı aracı.  
  
 Daha küçüktür ve IDE'de yük daha hızlı bir şekilde önceden çözümlenmiş bir profil oluşturma veri (.vsps) dosyası da oluşturabilirsiniz.  
  
> [!NOTE]
> Sembol (.pdb) dosyalarının kullanılabilir olduğundan emin olun **VSPerfReport**. Daha fazla bilgi için [nasıl yapılır: Komut satırından sembol dosyası konumlarını belirtme](../profiling/how-to-specify-symbol-file-locations-from-the-command-line.md).  
>   
> Yolu hakkında bilgi için **VSReport**, bkz: [komut satırı araçları yolunu belirtme](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).  
>   
> Profil oluşturma verilerinin bir .vsps dosyasında filtrelenemez.  
  
### <a name="to-embed-the-symbols-for-a-profiling-run-into-a-profiling-data-vsp-file"></a>Bir profil oluşturma veri (.vsp) dosyasına bir profil oluşturma için simgeleri eklemek için  
  
- Bir komut istemi penceresinde, aşağıdaki komutu yazın:  
  
   \<Yolu ><strong>VSPerfReport \<</strong> VSP dosyası > **packsymbols**  
  
   Varsayılan olarak, .vsp dosyasının temel adı ile .vsps dosyası olarak adlandırılır. Kullanarak bir diğer ad belirtebilirsiniz **çıkış** seçeneği.  
  
### <a name="to-create-a-summary-profiling-data-file"></a>Özet bir profil oluşturma veri dosyasını oluşturmak için  
  
- Bir komut istemi penceresinde, aşağıdaki komutu yazın:  
  
   \<Yolu ><strong>VSPerfReport \<</strong> VSP dosyası > **/summaryfile** [**/Output:**\<dosya adı >]  
  
   Varsayılan olarak, .vsp dosyasının temel adı ile .vsps dosyası olarak adlandırılır. Kullanarak bir diğer ad belirtebilirsiniz **çıkış** seçeneği.
