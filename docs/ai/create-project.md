---
title: Bir şablondan bir yapay ZEKA proje oluşturma
author: lisawong19
ms.author: liwong
manager: routlaw
ms.date: 11/13/2017
ms.topic: conceptual
ms.service: multiple
ms.workload:
- multiple
ms.openlocfilehash: e8b3f7a12b13c931513962a10d1eb5fcd4344174
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54786115"
---
# <a name="create-an-ai-project-from-a-template-in-visual-studio"></a>Visual Studio'da bir şablondan bir yapay ZEKA projesi oluşturma

Kaydederler [yapay ZEKA için Visual Studio Araçları yüklü](installation.md), çeşitli şablonları kullanarak yeni bir yapay ZEKA projesi oluşturmak daha kolaydır.

1. Visual Studio'yu başlatın.

2. Seçin **Dosya > Yeni > Proje** (Ctrl + Shift + N). İçinde **yeni proje** iletişim, arama "**yapay ZEKA Araçları**" ve istediğiniz şablonu seçin. Bir şablon seçerek hangi şablon sağlar kısa bir açıklama görüntüler unutmayın.

    ![Python şablonu içeren VS2017 yeni proje iletişim kutusu](media/create-project/new-ai-project.png)

3. Bu hızlı başlangıçta seçin "**TensorFlow uygulama**" şablonu, projeye bir ad (örneğin, "MNIST") ve konum verin ve seçin **Tamam**.

4. Visual Studio Proje dosyası oluşturur (bir `.pyproj` diskteki dosyanın) birlikte şablon tarafından açıklanan diğer dosyaları. "TensorFlow uygulama" şablonuyla proje projeniz gibi aynı adlı bir dosya içeriyor. Dosya varsayılan olarak Visual Studio düzenleyicisinde açın.

    ![Python uygulaması şablonu kullanılarak elde edilen proje](media/create-project/new-tensorflowapp.png)

5. Kod, TensorFlow, numpy sys ve işletim sistemi dahil olmak üzere birden çok kitaplık zaten içeri aktarır dikkat edin. Ayrıca, uygulama hazır kolayca giriş eğitim verileri, çıkış modelleri ve günlük dosyalarının konumunu değiştirme etkinleştirmek için giriş bazı bağımsız değişkenler ile başlar. Birden çok işlem bağlamlarının (Azure dosya paylaşımı üzerindeki, yerel geliştirme kutusunda IE farklı dizin), iş göndermek için bu params yararlıdır.

6. Projenizi bu giriş parametreleri için komut satırı bağımsız değişkenleri otomatik olarak geçirerek uygulamanızda hata ayıklama kolaylaştırmak için oluşturulan bazı özellikler de vardır. **Sağ tıklayın** projenizi seçip **özellikleri**

    ![Özellikler](media/create-project/project-properties.png)

7. Tıklayın **hata ayıklama** betik bağımsız değişkenleri otomatik olarak görmek için sekmesinde eklendi. bunları girişinizi bulunduğu ve depolanan çıkış istediğiniz gerektiği gibi değiştirebilir.

    ![Özellikler](media/create-project//project-properties_1.png)

8. Ctrl + F5'e basarak veya seçerek programı çalıştırın **hata ayıklama > hata ayıklama olmadan Başlat** menüsünde. Sonuçları konsol penceresinde görüntülenir.
