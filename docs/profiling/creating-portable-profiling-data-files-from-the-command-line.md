---
title: Profil oluşturma veri dosyaları komut satırından taşınabilir oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 2ceb63a7-b835-4988-b756-2afc3fcc4808
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 01b373fbe8a9aa0d7154f03855bb95472edf6b28
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53959728"
---
# <a name="create-portable-profiling-data-files-from-the-command-line"></a>Komut satırından taşınabilir profil oluşturma veri dosyaları oluşturma
Profil oluşturma verilerini daha kolay paylaşım yapmak için kullanabileceğiniz [VSPerfReport](../profiling/vsperfreport.md) karşılaştığınız bir profil simgeleri eklemek için komut satırı aracı. *Vsp* dosya.  
  
 Önceden çözümlenmiş bir profil oluşturma verilerini de oluşturabilirsiniz (. *vsps*) küçük ve IDE'de yük daha hızlı bir şekilde dosya.  
  
> [!NOTE]
>  Simgenin emin olun (. *pdb*) dosyaları için kullanılabilir **VSPerfReport**. Daha fazla bilgi için [nasıl yapılır: Komut satırından sembol dosyası konumlarını belirtme](../profiling/how-to-specify-symbol-file-locations-from-the-command-line.md).  
>   
>  Yolu hakkında bilgi için **VSReport**, bkz: [komut satırı araçları yolunu belirtin](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).  
>   
>  Profil oluşturma verileri bir. *vsps* dosya olamaz tablolarda filtreleme yapılmaz.  
  
### <a name="to-embed-the-symbols-for-a-profiling-run-into-a-profiling-data-vsp-file"></a>Bir profil oluşturma verilerini bir profil oluşturma için simgeleri eklemek için (. *Vsp*) dosyası  
  
- Bir komut istemi penceresinde, aşağıdaki komutu yazın:  
  
   \<Yolu ><strong>VSPerfReport \<</strong> VSP dosyası > **packsymbols**  
  
   Varsayılan olarak. *vsps* dosyası taban adı ile adlandırılır. *Vsp* dosya. Kullanarak bir diğer ad belirtebilirsiniz **çıkış** seçeneği.  
  
### <a name="to-create-a-summary-profiling-data-file"></a>Özet bir profil oluşturma veri dosyasını oluşturmak için  
  
- Bir komut istemi penceresinde, aşağıdaki komutu yazın:  
  
   \<Yolu ><strong>VSPerfReport \<</strong> VSP dosyası > **/summaryfile** [**/Output:**\<dosya adı >]  
  
   Varsayılan olarak. *vsps* dosyası taban adı ile adlandırılır. *Vsp* dosya. Kullanarak bir diğer ad belirtebilirsiniz **çıkış** seçeneği.