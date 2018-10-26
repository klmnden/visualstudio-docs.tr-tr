---
title: Visual Studio 2017'de yükleme konumlarını değiştirme
description: Konumun indirme önbelleğini, paylaşılan bileşenler, SDK'ları ve araçları farklı sürücülere değiştirerek sistem sürücünüzdeki yükleme ayak izini azaltmak öğrenin.
ms.date: 05/07/2018
ms.technology: vs-acquisition
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- change installation locations for Visual Studio
- move installation files to different drives
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 887ebca8645ab30d6d284433baf58451ab10b80c
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49869385"
---
# <a name="change-the-installation-locations-in-visual-studio-2017"></a>Visual Studio 2017'de yükleme konumlarını değiştirme

**15.7 sürümündeki yeni**: indirme önbelleğini, paylaşılan bileşenler, SDK'ları ve araçları farklı sürücülere taşıyarak sistem sürücünüzde yükleme ayak izini azaltabilir.

İşte nasıl.

1. Visual Studio'yu yüklediğinizde seçin **yükleme seçenekleri** sekmesi.

   ![2017 - Visual Studio yükleme konumunu değiştirmek](media/installation-options-by-location.png "yükleme konumunu değiştirme")

   > [!IMPORTANT]
   > Yüklemeyi duraklatmak ve daha sonra sürdürün, Visual Studio kaldığı seçer. Diğer bir deyişle, hangi indirilmesi ve yüklenmesi gereken ve önceki sayıdan başlamaz, yükleme ilerleme durumunu uygular.

2. İçinde **Visual Studio IDE** bölümünde, varsayılanı kabul edin. Bu, çekirdek ürüne yükler ve Visual Studio'nun bu sürümüne özgü dosyaları içerir.

   > [!IMPORTANT]
   > Sistem sürücünüzdeki neden öneririz sistem sürücünüzde varsayılan konumu kabul bir katı hal sürücüsü (SSD), burada'nın ise: Visual Studio ile geliştirdiğinizde, okuma ve disk g/ç etkinliği artıran çok sayıda dosya, için yazma.  Yükü işlemek için hızlı sürücünüze seçmek idealdir.

3. İçinde **indirme önbelleğini** bölümünde, indirme önbelleğini Tut ve ardından işaretleyin veya işaretini kaldırın yapıp yapmayacağınıza karar **indirme önbelleğini tut** uygun şekilde. <br><br>İndirme önbelleğini tutmamaya karar verirseniz, konum yalnızca geçici olarak kullanılır. De, bu eylem etkilemez ya önceki yüklemelerinden dosyaları silin. (Tüm yükleme paketlerini temizlemek için önceki tesislerinize ayrı olarak değiştirmeniz gerekir.)

4. İçinde **indirme önbelleğini** bölümünde, yükleme dosyaları ve bildirimleri depolamak istediğiniz sürücüyü belirtin. <br><br>"C++ ile masaüstü geliştirme" iş yükünü seçin, örneğin, geçici olarak gereken boyut 1.58 yüklemesi tamamlandıktan hemen sonra serbest bırakılır sistem sürücüsünde GB'dir.

   > [!NOTE]
   > Dosyaları ilk sistem sürücünüzdeki geçici bir klasöre indirilir ve sonra Visual Studio doğrular ve ardından bunları indirme önbellek klasörüne taşır. daha sonra silinir. Farklı bir sürücü, indirme önbelleğini tut seçeneğini belirlerseniz, Visual Studio hala sistem sürücünüzdeki yükleme önbellek boyutu değerine eşdeğer olan disk alanı gerekir.
   > [!IMPORTANT]
   > Konum, ilk yükleme ile ayarlanır ve yükleyicisi kullanıcı arabirimini daha sonra değiştirilemez. Bunun yerine, şunları yapmalısınız [komut satırı parametrelerini](use-command-line-parameters-to-install-visual-studio.md) indirme önbelleğini taşımak için

5. İçinde **paylaşılan bileşenler, Araçlar ve SDK'lar** bölümünde, yan yana Visual Studio yüklemeleri tarafından paylaşılan dosyaları depolamak istediğiniz sürücüyü belirtin. SDK'lar ve Visual Studio yükleyicisi olanak tanıyan Araçlar Ayrıca bu dizinde depolanan yükleme konumunu değiştirin.

   > [!NOTE]
   > Bazı araçlar vardır ve burada olabilir farklı kurallara sahip bir SDK'ları yüklenir. Başka bir konum seçin olsa bile bu araçlar ve SDK'lar yine de sistem sürücünüzde yüklenecektir.)

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio 2017'yi Yükleme](install-visual-studio.md)
* [Visual Studio 2017 güncelleştirmesi](update-visual-studio.md)
* [Visual Studio 2017'yi Değiştirme](update-visual-studio.md)
* [Visual Studio 2017'yi kaldırın](uninstall-visual-studio.md)
