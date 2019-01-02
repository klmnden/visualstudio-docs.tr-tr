---
title: 'Nasıl Yapılır: Ön ve son izleme komutları belirtme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.property.instrument
helpviewer_keywords:
- profiling tools, pre-instrument events
- events [Visual Studio], pre-instrument
- pre-instrument events, performance tools
ms.assetid: 6a8d5340-1d1b-4d81-88dd-8e1f435eb828
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c80e16b3566fd0687b74c5a43363864038f88cbf
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53861468"
---
# <a name="how-to-specify-pre--and-post-instrument-commands"></a>Nasıl Yapılır: Ön ve son izleme komutları belirtme

Önce veya sonra performans oturumu içindeki ikili dosyaları notınstrumented çalışan komutlar belirtebilirsiniz. Komut satırından verilen herhangi bir komutu bir işaretleme öncesi veya izleme sonrası olayı olarak belirtilebilir. Örneğin, ikili dosyaları algılayıcılarla sonra çalıştırılan bir toplu iş dosyasında bir tanımlayıcı ad anahtarıyla bir derlemenin bildirimin otomatikleştirmek komutları belirtebilirsiniz.

Komutları için profil oluşturma çalıştırmasını tüm izleme eklenmiş ikili dosyaları veya bireysel ikili dosyaları belirtebilirsiniz. Bununla birlikte, önce çalıştırmak için yalnızca bir işaretleme öncesi komutu ve izleme işleminden sonra çalıştırmak için yalnızca bir son izleme komut belirtebilirsiniz. Komutları bireysel ikili dosyaları ve hem tüm ikili dosyaları için belirtilemez. Tüm ikili dosyaları için komutları belirttiğinizde, önce veya sonra her bir ikili izleme oturumunda komutları çalıştırılır.

Komutları yürütülürken çalışma dizini çalıştırdığınız işletim sistemine bağlıdır [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] ve profili oluşturulan uygulamanın hedef platformu.

Profil oluşturma araçları için olan yolu almak için bkz: [komut satırı araçları yolunu belirtin](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md).

## <a name="to-specify-pre-instrument-commands"></a>İşaretleme öncesi komut belirtmek için

1. Aşağıdaki adımlardan birini uygulayın:

    - İşaretleme öncesi komutlar tüm ikili dosyaları için bir performans oturumu belirtmek için performans oturumu düğümünde seçin **performans Gezgini**ve ardından sağ tıklayıp **özellikleri**.

    - İşaretleme öncesi komut için belirli bir ikili belirtmek için ikili adına sağ tıklayın **hedefleri** performans oturumu tıklayın ve ardından listesi **özellikleri**.

2. İçinde **özellik sayfaları**, tıklayın **izleme**.

3. Komut türü **komut satırı** metin kutusu altında **işaretleme öncesi olaylar**.

    > [!NOTE]
    > Üç nokta düğmesine tıklayabilirsiniz **(...)**  bitişik olan **komut satırı** kutusunu göz atın ve uygun .exe, .cmd veya .bat dosyasını seçin.

4. **Tamam**'ı tıklatın.

     Komut çalışmasını kaldırmadan devre dışı bırakmak için seçin **İzleme'den Dışla** onay kutusu. Derleyici veya bağlayıcı ayarları değiştirmek için proje özellik sayfalarını kullanın.

## <a name="to-specify-post-instrument-commands"></a>Son izleme komutları belirtmek için

1. Aşağıdaki adımlardan birini uygulayın:

    - Son izleme komutları tüm ikili dosyaları için bir performans oturumu belirtmek için performans oturumu düğümünde seçin **performans Gezgini**ve ardından sağ tıklayıp **özellikleri**.

    - Son izleme komutları için belirli bir ikili belirtmek için ikili adına sağ tıklayın **hedefleri** performans oturumu tıklayın ve ardından listesi **özellikleri**.

2. İçinde **özellik sayfaları**, tıklayın **izleme**.

3. Komut türü **komut satırı** metin kutusu altında **son izleme olayları**.

    > [!NOTE]
    > Üç nokta düğmesine tıklayabilirsiniz **(...)**  bitişik olan **komut satırı** kutusunu göz atın ve uygun .exe, .cmd veya .bat dosyasını seçin.

4. **Tamam**'ı tıklatın.

     Komut çalışmasını kaldırmadan devre dışı bırakmak için seçin **İzleme'den Dışla** onay kutusu. Derleyici veya bağlayıcı ayarları değiştirmek için proje özellik sayfalarını kullanın.

## <a name="see-also"></a>Ayrıca bkz.

[Performans oturumlarını yapılandırma](../profiling/configuring-performance-sessions.md)
