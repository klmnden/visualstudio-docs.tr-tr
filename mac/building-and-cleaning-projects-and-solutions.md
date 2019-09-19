---
title: Projeleri ve Çözümleri Oluşturma ve Temizleme
description: Bu makalede Mac için Visual Studio içinde bir projenin nasıl oluşturulacağı açıklanır
author: heiligerdankgesang
ms.author: dominicn
ms.date: 09/19/2019
ms.assetid: E4B6CB42-9FE2-43B9-93B7-BD4BD50518B1
ms.openlocfilehash: 924bdb08154ecb3caad04cabf7e860bed9204e98
ms.sourcegitcommit: 53bc4c11b82882ab658e34c65ae374060f823531
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71128450"
---
# <a name="building-and-cleaning-projects-and-solutions"></a>Projeleri ve çözümleri oluşturma ve Temizleme

Bir çözümdeki projelerin tümünü veya bir kısmını oluşturma, yeniden oluşturma veya temizleme hakkında bilgi edinmek için bu makaledeki adımları izleyin.

> [!NOTE]
> Bu konu Mac için Visual Studio için geçerlidir. Windows üzerinde Visual Studio için bkz. [Visual Studio 'da projeler ve çözümler oluşturma ve Temizleme](/visualstudio/ide/building-and-cleaning-projects-and-solutions-in-visual-studio).

## <a name="to-build-rebuild-or-clean-an-entire-solution"></a>Derleme, yeniden oluşturmanız veya bütün bir çözüm Temizle

1. **Çözüm bölmesi**çözüm düğümünü seçin:

    ![Çözüm düğümünü seçme](media/compiling-and-building-image1.png)

2. Menü çubuğunda **Yapı** menüsünü seçin ve aşağıdaki seçeneklerden birini belirleyin:

    ![Tümünü Oluştur menü öğesi seçiliyor](media/compiling-and-building-image2.png)

    * En son derlemeden bu yana değiştirilen proje içindeki dosya ve bileşenleri derlemek için **Tümünü derle** ' yi seçin.

    * Çözümü "temizlemek" için **tümünü yeniden derle** ' yi seçin ve ardından tüm proje dosyalarını ve bileşenlerini derleyin.

    * Tüm ara ve çıkış dosyalarını silmek için **Tümünü Temizle** ' yi seçin. Yalnızca proje ve bileşen dosyalarını sol yeni örneklerini Ara ve Çıkış dosyalarını sonra oluşturulabilir.

## <a name="to-build-or-rebuild-a-single-project"></a>Derleme veya tek projeyi yeniden derleyin

1. **Çözüm bölmesi**projeyi seçin.

2. Menü çubuğundan **Yapı** menüsünü seçin.

3. Build [ProjectName], Rebuild [ProjectName] veya Clean [ProjectName] öğesini seçin.

## <a name="to-stop-a-build"></a>Bir derlemeyi durdurmak için

Bir derlemeyi durdurmak için, aşağıdaki seçeneklerden birini kullanın:

* Durum alanında kırmızı kareye basın:

    ![Derlemeyi durdurmak için kırmızı kare tuşuna basın](media/compiling-and-building-image3.png)

* **Derleme** menüsündeki **Durdur** öğesini kullanın.

* **Cmd + SHIFT + Return**tuşlarına basın.

## <a name="see-also"></a>Ayrıca bkz.

- [Projeleri ve çözümleri oluşturma ve Temizleme (Windows üzerinde Visual Studio)](/visualstudio/ide/building-and-cleaning-projects-and-solutions-in-visual-studio)