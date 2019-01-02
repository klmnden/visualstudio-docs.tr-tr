---
title: 'Nasıl Yapılır: Betiğe ekleme | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- script debugging, attaching to script
- script, attaching to
- processes, attaching to script
- remote debugging, attaching to script
ms.assetid: 82013e9a-ef53-4fd2-b451-a6891cdc6307
caps.latest.revision: 26
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e0fbdbf31c4ff504011a4ab80d50746d87ac3dac
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53858032"
---
# <a name="how-to-attach-to-script"></a>Nasıl Yapılır: Betiğe ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu konuda, bir komut dosyası hata ayıklama için Visual Studio hata ayıklayıcısını el ile ekleme açıklanmaktadır.  
  
### <a name="to-attach-to-a-running-process"></a>Çalışan bir işleme iliştirmek için  
  
1. Üzerinde **hata ayıklama** menüsünde seçin **iliştirme**. (Hiçbir proje açıksa seçin **iliştirme** üzerinde **Araçları** menü.)  
  
2. İçinde **iliştirme** iletişim kutusu, göz **kullanılabilir işlemler** listesi ve bulma komut dosyası işleme iliştirmek istediğiniz. Betik işlemleri bakarak belirleyebilirsiniz **türü** sütun.  
  
   1.  Hata ayıklama yapmak istediğiniz işlemi başka bir bilgisayarda çalışıyorsa, uzak bilgisayarın seçmeniz gerekir. Daha fazla bilgi için [nasıl yapılır: Uzak bilgisayar seçme](http://msdn.microsoft.com/en-us/4332ba8e-2f0b-4f62-b96a-e762b9f3c3ba).  
  
   2.  İşlemi farklı bir kullanıcı hesabı altında çalışıyorsa, seçin **tüm kullanıcıların işlemlerini göster** onay kutusu.  
  
   3.  Aracılığıyla bağlanırsanız **Uzak Masaüstü Bağlantısı**seçin **tüm oturumlardaki işlemleri göster** onay kutusu.  
  
3. Eklemek istediğiniz işlemi tıklayın.  
  
4. İçinde **ekleme** kutusunda, görmelisiniz **betik kodu** veya **otomatik: Betik kodu**. Başka bir şey görürseniz, aşağıdaki adımları izleyin:  
  
   1.  Tıklayın **seçin**.  
  
   2.  İçinde **kod türünü seç** iletişim kutusu, tıklayın **bu tür kodlarda hata ayıklama** seçip **betik**.  
  
   3.  **Tamam**'ı tıklatın.  
  
5. Tıklayın **ekleme**.  
  
    Bu noktada, komut dosyası hata ayıklaması Internet Explorer'da devre dışı bırakıldığını belirten bir uyarı görebilirsiniz. Bu meydana gelirse, bkz. [uyarısı: Betik hata ayıklaması devre dışı](../debugger/warning-script-debugging-disabled.md).  
  
   **Kullanılabilir işlemler** listesi açıldığında otomatik olarak görüntüleniyor **işlemleri** iletişim kutusu. İşlemler başlatabilir ve iletişim kutusu açıkken arka planda durdurabilirsiniz. Bu nedenle, içeriği her zaman güncel olmayabilir. Listenin tuşlarına basarak işlemlerin geçerli listesini görmek için herhangi bir zamanda yenileyebilirsiniz **Yenile** düğmesi.  
  
   Birden çok programları için hata ayıklama, ancak herhangi bir anda yalnızca bir programı hata ayıklayıcıda etkin eklenebilir. Hata ayıklama konumu araç çubuğunda etkin programı ayarlayabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Geçerli süreci Ayarla](http://msdn.microsoft.com/en-us/7e1d7fa5-0e40-44cf-8c41-d3dba31c969e).  
  
   Tüm **hata ayıklama** yürütme komutlarını etkin programı etkiler. Herhangi bir hata ayıklaması yapılan programa işlemleri iletişim kutusundan bozabilir. Bkz: [kesme noktalarını kullanma](../debugger/using-breakpoints.md).  
  
> [!NOTE]
>  Güvenilmeyen bir kullanıcı tarafından sahip olunan bir işlem eklemeye çalışırsanız, bir güvenlik uyarısı iletişim kutusu onayı görünecektir. Daha fazla bilgi için [güvenlik uyarısı: Güvenilmeyen bir kullanıcının sahip olduğu işleme ekleme tehlikeli olabilir. Aşağıdaki bilgiler kuşkulu görünüyorsa ya da emin değilseniz, bu işleme eklemeyin](/visualstudio/debugger/security-warning-attaching-to-a-process-owned-by-an-untrusted-user?view=vs-2015).  
  
 Bazı durumlarda, bir Terminal Hizmetleri (Uzak Masaüstü) oturumunda hata ayıklaması yapıyorsanız kullanılabilir işlemler listesi kullanılabilir tüm işlemleri görüntülemez. Üzerinde [!INCLUDE[WinXPSvr](../includes/winxpsvr-md.md)] veya sonraki sürümleri, Visual Studio sınırlı bir kullanıcı olarak çalıştırıyorsanız kullanılabilir işlemler listesi gösterilmez Hizmetleri için kullanılan oturum 0'da çalışan işlemler ve w3wp.exe dahil olmak üzere diğer sunucu işlemleri. Visual Studio'yu bir yönetici hesabı altında çalışan veya Visual Studio, bir Terminal Hizmetleri oturumu yerine sunucu konsolunun çalıştırarak sorunu çözebilirsiniz. Bu geçici çözümlerden biri Mümkünse, üçüncü seçenek olmasına vsjitdebugger.exe yazarak işlemine eklemek için Windows komut satırınalodctr ProcessId -p. Tlist.exe kullanarak işlem kimliğini belirleyebilirsiniz. Tlist.exe'yi edinmek için indirme ve hata ayıklama araçları için Windows, kullanılabilir yükleme [Windows Donanım Geliştirme Merkezi](http://go.microsoft.com/fwlink/?linkid=1651).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İstemci tarafı betikte hata ayıklama](../debugger/client-side-script-debugging.md)   
 [Çalıştırma işlemleri iliştirme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md)   
 [Güvenlik Uyarısı: Güvenilmeyen bir kullanıcının sahip olduğu işleme ekleme tehlikeli olabilir. Aşağıdaki bilgiler kuşkulu görünüyorsa ya da emin değilseniz, bu işleme eklemeyin.](/visualstudio/debugger/security-warning-attaching-to-a-process-owned-by-an-untrusted-user?view=vs-2015)   
 [Hata Ayıklayıcısı Güvenliği](../debugger/debugger-security.md)



