---
title: Mevcut koddan bir yapay ZEKA projesi oluşturma
author: lisawong19
ms.author: liwong
manager: routlaw
ms.date: 11/13/2017
ms.topic: conceptual
ms.service: multiple
ms.workload:
- multiple
ms.openlocfilehash: a2a09fd3214cddf4f63fd2c32874db5b67a9b9dc
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54760445"
---
# <a name="create-an-ai-project-from-existing-code"></a>Mevcut koddan bir yapay ZEKA projesi oluşturma

Kaydederler [yapay ZEKA için Visual Studio Araçları yüklü](installation.md), varolan bir Python kodu bir Visual Studio projesine getirmek kolaydır.

> [!Important]
> Burada açıklanan işlemi taşıma veya kopyalama orijinal kaynak dosyalarına desteklemez. Bir kopya ile çalışmak istiyorsanız, klasörü ilk çoğaltma.

1. Visual Studio'yu başlatın ve seçin **Dosya > Yeni > Proje**.

2. İçinde **yeni proje** iletişim, arama "**yapay ZEKA Araçları**" seçin "**alanından mevcut Python kodu**" Şablon, proje adını ve konumunu verin ve seçin**Tamam**.

   ![Yeni Proje varolan koddan 1. adım](media/create-project-existing/new-ai-project.png)

3. Görüntülenen sihirbazında, mevcut kodunuzu yolunu ayarlama, dosya türleri için bir filtre ayarlayın ve projenize gerektirir ve ardından arama yolları belirtin **Tamam**. Hangi arama yolları bilmiyorsanız, bu alanı boş bırakın.

   ![Yeni Proje varolan koddan 2. adım](media/create-project-existing/azurebatch-newproject.png)

   Mevcut kodunuzu Azure Machine Learning projesinin bir parçasıysa denetleyin **olan Azure Machine Learning klasör** deneme gibi önemli Azure Machine Learning yapılandırma ayrıntıları başarıyla dönüştürülmesini sağlamak için Hesap, işlem bağlamları kullanmak için çalışma alanı ve daha fazlası.

4. Bir başlangıç dosyası ayarlamak için dosyada bulun **Çözüm Gezgini**, sağ tıklatın ve seçin **başlangıç dosyası olarak ayarla**.

5. Tuşlarına basarak programı çalıştırın **Ctrl**+**F5** veya seçerek **hata ayıklama > hata ayıklama olmadan Başlat**.

> [!div class="nextstepaction"]
> [Öğretici: Visual Studio'da Python ile çalışma](../python/tutorial-working-with-python-in-visual-studio-step-00-installation.md)

## <a name="see-also"></a>Ayrıca bkz.

- [El ile bir Python ortamı tanımlayın](../python/managing-python-environments-in-visual-studio.md#manually-identify-an-existing-environment)