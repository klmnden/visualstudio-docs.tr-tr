---
title: Profil oluşturma ve Windows Vista güvenliği | Microsoft Docs
ms.date: 11/02/2018
ms.topic: conceptual
helpviewer_keywords:
- Profiling Tools,security
- performance tools, security
ms.assetid: 842112fc-b886-4801-8cd7-a25b314b0393
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 091961f3425714c0dc5ddabfac847c76339ab064
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55025574"
---
# <a name="profiling-and-windows-vista-security"></a>Profil oluşturma ve Windows Vista güvenliği

Yapılandırmanıza bağlı olarak [!INCLUDE[wiprlhext](../debugger/includes/wiprlhext_md.md)] bilgisayar yöneticisi kullanılabilir hale getirdiği kullanıcı erişimi izinleri ayarları, bireysel bir kullanıcı bu bilgisayarda bir işlem profili için güvenlik izni olabilir. Aşağıdaki örneklerde kullanıcılar arasındaki olası farklar gösterilmektedir:

- Yöneticisi hizmetinin başlatılmasını ve sürücü ayarladığınızda, bazı kullanıcılar Gelişmiş profil oluşturma özelliklerine erişebilir.

- Etki alanı kullanıcıları yalnızca örnek profil oluşturma erişebilir.

- Bazı kullanıcılar, diğer tüm kullanıcılar için profil oluşturma için erişim reddedebilir.

  Daha fazla bilgi için yönetim seçenekleri görmek [VSPerfCmd](../profiling/vsperfcmd.md).

## <a name="cross-session-profiling"></a>Çapraz oturum profil oluşturma

*Çapraz oturum profil oluşturma* farklı kullanıcı oturumunda çalışan bir işlemi profil yeteneğidir. Örneğin, çoğu Hizmetleri 0 oturumunda çalıştırın ve kullanıcıların 0. oturumunda doğrudan çalıştıramazsınız. Kullanarak **iliştirme** performans Gezgini araç çubuğundan veya `/attach` seçeneği VSPerfCmd komut satırı aracı, farklı bir kullanıcı oturumunu çoğu işlemlerin profilini oluşturabilirsiniz.

Çapraz işlem profil görünürlüğü seçeneklerini ayarlayarak kullanılabilir işlem listesini görebilirsiniz. Bu seçenekler kullanılabilir **iliştirme** seçeneğini belirlediğinizde görüntülenen penceresi **iliştirme**:

- **Tüm kullanıcıların işlemlerini göster**

  Bu seçeneği seçili değilse, listeyi yalnızca geçerli kullanıcıya ait işlemleri görüntüler. Aksi takdirde, tüm kullanıcıların işlemlerini listeler.

- **Tüm oturumlardaki işlemleri göster**

  Bu seçeneği seçili değilse, listenin geçerli oturumda işlemleri görüntüler. Aksi takdirde, listenin tüm oturumlardaki işlemleri görüntüler.

## <a name="see-also"></a>Ayrıca bkz.

- [Genel Bakışlar](../profiling/overviews-performance-tools.md)
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Nasıl yapılır: Çalışan bir işleme](/previous-versions/visualstudio/visual-studio-2010/c6wf8e4z\(v\=vs.100\))
