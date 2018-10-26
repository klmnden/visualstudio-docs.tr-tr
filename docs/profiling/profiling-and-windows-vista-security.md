---
title: Profil oluşturma ve Windows Vista güvenliği | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Profiling Tools,security
- performance tools, security
ms.assetid: 842112fc-b886-4801-8cd7-a25b314b0393
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ac83bc523b830c3e3adff258511d2785db0ddb62
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49924804"
---
# <a name="profiling-and-windows-vista-security"></a>Profil Oluşturma Windows Vista Güvenliği
Yapılandırmanıza bağlı olarak [!INCLUDE[wiprlhext](../debugger/includes/wiprlhext_md.md)] bilgisayar yöneticisi kullanılabilir hale getirdiği kullanıcı erişimi izinleri ayarları, bireysel bir kullanıcı bu bilgisayarda bir işlem profili için güvenlik izni olabilir. Aşağıdaki örneklerde kullanıcılar arasındaki olası farklar gösterilmektedir:  
  
- Yöneticisi hizmetinin başlatılmasını ve sürücü ayarladığınızda, bazı kullanıcılar Gelişmiş profil oluşturma özelliklerine erişebilir.  
  
- Etki alanı kullanıcıları yalnızca örnek profil oluşturma erişebilir.  
  
- Bazı kullanıcılar, diğer tüm kullanıcılar için profil oluşturma için erişim reddedebilir.  
  
  Daha fazla bilgi için yönetim seçenekleri görmek [VSPerfCmd](../profiling/vsperfcmd.md).  
  
## <a name="cross-session-profiling"></a>Çapraz oturum profil oluşturma  
 *Çapraz oturum profil oluşturma* farklı oturumda çalışan bir işlemi profil yeteneğidir. Örneğin, çoğu Hizmetleri 0 oturumunda çalıştırın ve kullanıcıların 0. oturumunda doğrudan çalıştıramazsınız. Kullanarak **iliştirme** performans Gezgini araç çubuğundan veya / komut satırı aracının VSPerfCmd seçenek ekleme, çoğu işlemleri farklı oturum açılışlarında profil oluşturabilirsiniz.  
  
 Çapraz işlem profil görünürlüğü seçeneklerini ayarlayarak kullanılabilir işlem listesini görebilirsiniz. Bu seçenekler kullanılabilir **iliştirme** tıkladığınızda görüntülenen penceresi **iliştirme**:  
  
-   **Tüm kullanıcıların işlemlerini göster**  
  
     Bu seçenek, yalnızca geçerli kullanıcıya ait işlemler listede görüntülenir. Zaman **tüm kullanıcıların işlemlerini göster** olduğu belirlenirse, tüm kullanıcıların işlemlerini listesini görüntüler.  
  
-   **Tüm oturumlardaki işlemleri göster**  
  
     Bu seçenek seçilmezse, listenin geçerli oturumda işlemleri görüntüler. Bu seçenek belirlendiğinde, listenin tüm oturumlardaki işlemleri görüntüler.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Genel bakış](../profiling/overviews-performance-tools.md)   
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Nasıl yapılır: çalışan bir işleme](http://msdn.microsoft.com/en-us/636d0a52-4bfd-48d2-89ad-d7b9ca4dc4f4)