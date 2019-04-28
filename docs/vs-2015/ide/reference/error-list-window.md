---
title: Hata Listesi penceresi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- VS.ErrorList
helpviewer_keywords:
- Task List
- build errors
- Error List window
- errors [Visual Studio], Error List window
ms.assetid: b7f6d45a-733b-4ad8-bc2f-737a37509e56
caps.latest.revision: 36
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 924e4414d668f4cb3a12f5d27b915117da0a7119
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63437222"
---
# <a name="error-list-window"></a>Hata Listesi Penceresi
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

[NOT]
> Hata listesi, belirli bir hata iletisi hakkındaki bilgileri görüntüler. Hata numarasını veya hata dizesi metnini çıktı penceresinden kopyalayabilirsiniz. Çıktı penceresini görüntülemek için Ctrl + Alt + O tuşlarına basın. Bkz: [çıkış penceresi](../../ide/reference/output-window.md).  
  
 Kullanarak uygulamalarınızı daha hızlı geliştirebilirsiniz **hata listesi** penceresi. Örneğin, aşağıdaki görevleri gerçekleştirebilirsiniz:  
  
- Hatalar, uyarılar ve kod yazdığınız sırada üretilen iletileri görüntüleyin.  
  
- IntelliSense tarafından fark edilen sözdizimi hatalarını bulur.  
  
- Bulma dağıtım hatalarını, belirli statik analiz hatalarını ve kurumsal şablon ilkeleri uygulanırken saptanan hataları.  
  
- Burada sorun ortaya çıkar ve hata konumuna gitmek dosyayı açmak için hata iletisini çift tıklayın.  
  
- Hangi girişlerin görüntüleneceğini ve her giriş için hangi bilgi sütunlarını görünür filtreleyin.  
  
- Özel terimleri arayın ve yalnızca geçerli proje veya belgeyi aramayı kapsamına.  
  
  Görüntülenecek **hata listesi**, tıklayın **görünüm / hata listesinde**, veya **CTRL +\\+ E**.  
  
  Seçebileceğiniz **hataları**, **uyarıları**, ve **iletileri** farklı düzeylerde bilgileri görmek için sekmeler.  
  
  Listeyi sıralamak için herhangi bir sütun başlığına tıklayın. Başka bir sütuna göre yeniden sıralamak için SHIFT tuşunu basılı tutun ve başka bir sütun başlığına tıklayın. Hangi sütunların görüntülenip hangilerinin gizlendiğini seçmek için seçin **sütunları göster** kısayol menüsünden. Sütunların görüntülenme sırasını değiştirmek için herhangi bir sütun başlığını sola veya sağa sürükleyin.  
  
> [!NOTE]
> İletişim kutuları ve menü komutları gördüğünüz, etkin ayarlarınıza ve sürüm bağlı olarak burada açıklananlar farklılık gösterebilir. Ayarlarınızı değiştirmek için tıklayın **Araçlar / içe ve dışa aktarma ayarları**. Daha fazla bilgi için [Visual Studio'da geliştirme ayarlarını özelleştirme](http://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
## <a name="error-list-filters"></a>Hata listesi filtreleri  
 Araç çubuğunun sağ tarafında biri diğeri araç çubuğunun solunda iki açılır liste kutusu filtrede iki tür vardır. Araç çubuğunun sol tarafta açılır listeden kullanılacak kod dosyalarını belirtir (**çözümün tamamında**, **açık belgeler**, **geçerli proje**,  **Geçerli belge**).  
  
 Analiz etmek ve hata grupları üzerinde hareket için arama kapsamını sınırlandırabilirsiniz. Örneğin, bir projenin derlenmesini önleyen çekirdek hatalarına odaklanmak isteyebilirsiniz. Kapsam belirleme seçenekleri şunlardır:  
  
1. **Açık belgeler**: Hataları, uyarıları ve iletileri açık belgelerin gösterir.  
  
2. **Geçerli proje**: Hataları, uyarıları ve iletileri seçilmiş belgenin projesinden **Düzenleyicisi** veya seçilen projede **Çözüm Gezgini**.  
  
   > [!NOTE]
   > Şu anda seçili olan belgenin projesi seçili projeden farklıysa, filtrelenmiş liste hataları, uyarıları ve iletileri değiştirecek **Çözüm Gezgini**.  
  
3. **Geçerli belge**: Hataları, uyarıları ve iletileri için seçilmiş belgenin içinde Göster **Düzenleyicisi** veya **Çözüm Gezgini**.  
  
   Bir filtre o anda arama sonucuna uygulanırsa, filtrenin adını görünür **hata listesi** başlık çubuğu. **Hataları**, **uyarıları**, ve **iletileri** düğmeleri sonra toplam öğe sayısının yanı sıra gösterilen filtrelenmiş öğe sayısını da görüntüler; örneğin, düğme Göster x / y hata. Hiçbir filtre uygulanmamışsa başlık çubuğunda yalnızca "hata listesi" yazar.  
  
   Araç çubuğunun sağ tarafındaki listenin (bir yapı işleminden kaynaklanan hatalar) derleme hatalarından gösterilip gösterilmeyeceğini belirtir veya IntelliSense (bir derleme çalıştırmadan önce algılanan hataları) veya her ikisi de.  
  
## <a name="search"></a>Ara  
 Kullanım **arama hatası listesi** metin kutusunun sağ alt tarafında **hata listesi** hata Listesi'nde belirli hataları bulmak için araç çubuğu. Hata listesindeki görünen herhangi bir sütunda arama yapabilirsiniz ve arama sonuçları her zaman sorgu veya uygulanan filtre yerine sıralama önceliği olan sütun göre sıralanır. Seçerseniz **Esc** odak modundayken anahtar **hata listesi**, arama terimini temizleyebilir ve arama sonuçlarını filtrelersiniz. Ayrıca **X** temizleyin metin kutusunun sağ tarafındaki.  
  
## <a name="save"></a>Kaydet  
 Hata listesini kopyalayabilir ve bir dosyaya kaydedin. Kopyala ve seçimi sağ tıklayın ve ardından bağlam menüsünde istediğiniz hataları seçin **kopyalama**. Ardından, hataları bir dosyaya yapıştırabilirsiniz. Hataları bir Excel elektronik tablosuna yapıştırırsanız, alanlar farklı sütunlar olarak görünür.  
  
## <a name="ui-element-list"></a>UI öğe listesi  
 Önem Derecesi  
 Farklı türde görüntüler **hata listesi** giriş (**hata**, **ileti**, **uyarı**, **uyarı (etkin)**, **(Devre dışı) uyarı**.  
  
 Kod  
 Hata kodu görüntülenir.  
  
 Açıklama  
 Giriş metni görüntüler.  
  
 Project  
 Geçerli projenin adını görüntüler.  
  
 Dosya  
 Dosya adını görüntüler.  
  
 Çizgi  
 Sorun oluştuğu satırı görüntüler.
