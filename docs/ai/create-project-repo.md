---
title: Bir depoyu kopyalama
author: lisawong19
ms.author: liwong
manager: routlaw
ms.date: 11/13/2017
ms.topic: conceptual
ms.service: multiple
ms.workload:
- multiple
ms.openlocfilehash: fd0c71e9f426c5591f9ac3ecd135c1b230ca5e20
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54986065"
---
# <a name="clone-a-repository-of-python-code-in-visual-studio"></a>Visual Studio'da Python kodunun bir depoyu kopyalama

Kaydederler [yapay ZEKA için Visual Studio Araçları yüklü](installation.md), kolayca Python kodu bir depoyu kopyalamak ve bir proje oluşturun.

1. Visual Studio Yükleyicisi'ni çalıştırın, GitHub depoları için bağlanmayı seçin **Değiştir**seçip **tek tek bileşenler** sekmesi. Ekranı aşağı kaydırarak **kod Araçları** bölümünden **Visual Studio için GitHub uzantısı**seçip **Değiştir**.

    ![Visual Studio Yükleyicisi'nde GitHub uzantısı seçme](media/create-project-repo/installation-github-extension.png)

2. Visual Studio'yu başlatın.

3. Seçin **Görüntüle > Takım Gezgini** açmak için **Takım Gezgini** penceresi içinde GitHub veya Azure DevOps bağlanabilir, ya da bir depoyu kopyalayın.

    ![Azure DevOps, GitHub'ı gösteren ve bir depo kopyalama Takım Gezgini penceresi](media/create-project-repo/team-explorer-devops.png)

4. Altında alanına **yerel Git depoları**, girin `https://github.com/Microsoft/samples-for-ai`, kopyalanan dosyalar için bir klasör girin ve seçin **kopya**.

    > [!Tip]
    > Takım Gezgini'nde belirttiğiniz klasör, kopyalanan dosyalar almak için belirli bir klasördür. Farklı `git clone` komutunu, Ekip Gezgini'nde bir kopya oluşturma otomatik olarak oluşturmaz bir alt klasör deponun adını.

5. Kopyalama tamamlandığında, Team Explorer'ı depo panosuna gitmek için sayfanın alt kısmında depo klasörü çift tıklatın. Altında **çözümleri**seçin **yeni**.

    ![Takım Gezgini penceresinde, bir kopya yeni proje oluşturma](media/create-project-repo/team-explorer-new-project.png)

6. İçinde **yeni proje** görüntülenen iletişim seçin "**ilk mevcut Python kodu**", proje için bir ad belirtin, Ayarla **konumu** deposu olarak aynı klasöre ve seçin **Tamam**. Açılan sihirbazda seçin **son**.

7. Seçin **Görüntüle > Çözüm Gezgini** menüsünde.

8. Çözüm Gezgini'nde `TensorFlow Examples> MNIST` düğümünü sağ `convolutional.py`seçip **başlangıç dosyası olarak ayarla**. Bu adım, Visual Studio projeyi çalışırken kullanması gereken hangi dosya söyler.

9. Tuşuna **Ctrl**+**F5** veya **hata ayıklama > hata ayıklama olmadan Başlat** programı çalıştırmak için. Bir hata görürseniz, önceki adımda çalışma dizini ayarı yeniden denetleyin.

10. Program başarıyla çalıştırıldığında, eğitim indirin ve veri kümesi, test sonra modeli eğitmek ve çıkış, hata oranı Başlat görürsünüz. İstediğiniz zaman içinde azaltmak için hata oranı

    ![İlk Python MNIST programının çıktısı](media/create-project-repo/tensorflow-mnist-running.png)

   > [!NOTE]
   > Anaconda kullanıyorsanız ve eksik numpy hakkında bir hata iletisi, gerekebilir [Anaconda kullanmak için Python ortamınız değiştirme](../python/selecting-a-python-environment-for-a-project.md).

11. İlerleme durumunu TensorBoard görselleştirebilirsiniz. Projenize sağ tıklayın ve tıklayın **çalıştırma TensorBoard** TensorBoard günlükleri çıkış dizini'ı seçin.

   ![tensorboard çalıştırın](media/create-project-repo/run-tensorboard.png)

12. Kaliteyi artırma anlamına gelir, zaman içinde azalan hata dikkat edin.

   ![tensorboard çalıştırın](media/create-project-repo/tensorboard.png)
