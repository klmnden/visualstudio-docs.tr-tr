---
title: Projeler ve çözümler, Seçenekler iletişim kutusu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- Projects and Solutions Options dialog box
- Options dialog box, Projects and Solutions
ms.assetid: 2801f24e-a138-488a-ae3c-e1f99a678ac0
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 2bdcfc2f6a4b7655a6f4f2e335310e938e5acfed
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65701977"
---
# <a name="projects-and-solutions-options-dialog-box"></a>Projeler ve Çözümler, Seçenekler İletişim Kutusu
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Varsayılan yolunu ayarlar [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] proje klasörleri ve varsayılan davranışını belirler **çıkış** penceresinde **görev listesi**, ve **Çözüm Gezgini** olarak projeleri geliştirilen ve derlenen. Bu iletişim kutusuna erişmek için tıklayın **Araçlar / Seçenekler** genişletin **projeler ve çözümler**, tıklatıp **genel**.  
  
> [!NOTE]
> İletişim kutuları, adları ve konumları gördüğünüz gibi menü komutlarının Seçenekleri Yardımı'nda, etkin ayarlarınıza ve sürüm bağlı olarak açıklanan nedir öğesinden farklı olabilir. Bu Yardım sayfası ile yazılmıştır **genel geliştirme ayarları** unutmayın. Ayarlarınızı değiştirmek veya görüntülemek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [Visual Studio'da geliştirme ayarlarını özelleştirme](https://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
## <a name="settings"></a>Ayarlar  
 **Projeleri konumu**  
 Yeni proje ve çözüm klasörleri ve dizinleri oluşturulduğu varsayılan konumunu ayarlar. Birçok iletişim kutusu da başlangıç noktaları klasörü için bu seçeneği ayarlamak konumu kullanın. Örneğin, Proje Aç iletişim kutusu için Projelerim kısayol bu konumu kullanır.  
  
 **Kullanıcı proje şablonları konumu**  
 Tarafından kullanılan varsayılan konumu ayarlar **yeni proje** listesini oluşturmak için iletişim kutusu **Şablonlarım**. Daha fazla bilgi için [nasıl yapılır: Şablonları bulma ve düzenleme](../../ide/how-to-locate-and-organize-project-and-item-templates.md).  
  
 **Kullanıcı öğe Şablonları konumu**  
 Tarafından kullanılan varsayılan konumu ayarlar **Yeni Öğe Ekle** listesini oluşturmak için iletişim kutusu **Şablonlarım**. Daha fazla bilgi için [nasıl yapılır: Şablonları bulma ve düzenleme](../../ide/how-to-locate-and-organize-project-and-item-templates.md).  
  
 **Hata listesi bir derleme hatayla bittiğinde her zaman göster**  
 Açılır **hata listesi** derleme tamamlandığında, yalnızca bir projeyi oluşturmak başarısız olursa penceresi. Derleme işlemi sırasında oluşan hatalar görüntülenir. Bu seçenek işaretli değilse, hataları oluşmaya ancak yapı tamamlandığında pencerenin açılmaz. Bu seçenek varsayılan olarak etkindir.  
  
 **Çözüm Gezgini'nde etkin öğeyi takip et**  
 Bu onay kutusu seçildiğinde, **Çözüm Gezgini** otomatik olarak açılır ve etkin öğeyi seçili. Seçili öğe değiştikçe, farklı bir proje veya çözüm dosyaları ya da farklı bileşenlerin bir tasarımcıda çalışın. Ne zaman bu seçenek işaretli değilse, seçimdeki **Çözüm Gezgini** otomatik olarak değiştirmez. Bu seçenek varsayılan olarak etkindir.  
  
 **Gelişmiş derleme yapılandırmalarını Göster**  
 Bu onay kutusu seçildiğinde, derleme yapılandırma seçenekleri görünür **proje özellik sayfaları** iletişim kutusu ve **çözüm özellik sayfaları** iletişim kutusu. Yapı yapılandırma seçeneklerini üzerinde görünmez temizlendiğinde **proje özellik sayfaları** iletişim kutusu ve **çözüm özellik sayfaları** iletişim kutusu için [!INCLUDE[vbprvb](../../includes/vbprvb-md.md)] ve [!INCLUDE[csprcs](../../includes/csprcs-md.md)] projeleri bir yapılandırma veya iki yapılandırması hata ayıklama ve yayın içeren. Kullanıcı tanımlı bir yapılandırma bir proje varsa, yapı yapılandırma seçenekleri gösterilmektedir.  
  
 Seçili üzerinde olmadığında komutları **derleme** menüsünde gibi **Çözümü Derle**, **çözümü yeniden derle**, ve **çözümü Temizle**, olan Yayın yapılandırması ve komutları üzerinde gerçekleştirilen **hata ayıklama** menüsünde gibi **hata ayıklamayı Başlat** ve **hata ayıklama olmadan Başlat**, gerçekleştirilir hata ayıklama yapılandırması.  
  
 **Çözümü her zaman göster**  
 Bu onay kutusu seçildiğinde, çözüm ve çözümler üzerinde çalışan tüm komutları her zaman IDE'de gösterilir. Bu onay kutusu temizlenirse, tüm projeler tek başına bir proje olarak oluşturulur ve çözümü yalnızca bir proje içeriyorsa, Çözüm Gezgini veya hareket komutları çözümde IDE'de çözümler üzerinde görmezsiniz.  
  
 **Oluşturulduğunda yeni projeleri Kaydet**  
 Bu onay kutusu seçildiğinde, projeniz için bir konum belirtebilirsiniz **yeni proje** iletişim kutusu. Bu onay kutusu temizlenirse, tüm yeni projeler geçici proje olarak oluşturulur. Geçici projeler ile çalışırken, oluşturabilir ve bir disk konumu belirtmek zorunda kalmadan bir proje ile denemeler yapın.  
  
 **Proje konumu güvenilir olmadığında kullanıcıyı uyarır.**  
 Yeni bir proje oluşturun veya tam olarak (örneğin, bir UNC yolu veya HTTP yolu) güvenli olmayan bir konumda mevcut bir projeyi açmayı denerseniz, bir ileti görüntülenir. İleti oluşturmak veya tam olarak güvenilmeyen bir konumda bir projeyi açmayı denemek her zaman görüntülenip görüntülenmeyeceğini belirtmek için bu seçeneği kullanın.  
  
 **Derleme başladığında çıkış penceresini göster**  
 Otomatik olarak çıktı penceresinde çözümünün gizliliğe IDE görüntüler oluşturur. Daha fazla bilgi için [nasıl yapılır: Çıkış penceresini denetleme](https://msdn.microsoft.com/library/91aebd15-8854-4a7a-9f7d-57376fb4e858). Bu seçenek varsayılan olarak etkindir.  
  
 **Sembolik yeniden adlandırmayı olduğunda yeniden adlandırmayı sor**  
 Bu onay kutusu seçildiğinde, isteyen bir ileti kutusu görüntüler olup olmadığını [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] projedeki tüm başvuruları kod öğesine de yeniden adlandırmanız gerekir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Seçenekler İletişim Kutusu, Projeler ve Çözümler, Derleme ve Çalıştırma](../../ide/reference/options-dialog-box-projects-and-solutions-build-and-run.md)
