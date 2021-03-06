---
title: Proje ve Çözüm Özelliklerini Yönetme
description: Bu makaleler, Mac için projeler ve çözümler Visual Studio'da özelliklerini yönetmek nasıl açıklar
author: heiligerdankgesang
ms.author: dominicn
ms.date: 05/06/2018
ms.assetid: 75247EB8-323A-4AFD-A451-6703A03D5D1F
ms.openlocfilehash: 514792804515541b7e4f64359a08e9c6093c5018
ms.sourcegitcommit: 7fbfb2a1d43ce72545096c635df2b04496b0be71
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/09/2019
ms.locfileid: "67692879"
---
# <a name="managing-project-and-solution-properties"></a>Proje ve Çözüm Özelliklerini Yönetme

## <a name="project-options"></a>Proje seçenekleri

Proje seçenekleri, her proje için özeldir ve proje nasıl yazılır, yerleşik ve çalıştırma etkiler. (Bu kullanıcıya özgü seçenekleri ayarlar) Mac tercihleri ve (hangi çözümün tamamını seçeneklerini ayarlama) çözüm seçenekleri için Visual Studio ile karşılaştırır. Diğer geliştiriciler oluşturabilir ve doğru projeyi çalıştırın, proje seçenekleri proje (.csproj) dosyasında depolanır. Belirli proje seçenekleri dosyanın biçimlendirmesini ödün vermeden aynı belge üzerinde çalışmak birçok geliştiricinin sağlar.

Mac için Visual Studio'da proje Seçenekleri'ni açmak için proje adına çift tıklayın veya bağlam menüsünü açmak için sağ tıklayın ve ardından **seçenekleri**:

![Bağlam menüsü seçeneği](media/projects-and-solutions-image2.png)

Düzenlenebilir seçenekleri, çalıştırın ve kaynak kodu ve sürüm denetimi kümesi oluşturmak için seçenekleri içerir.

Proje seçenekleri beş farklı kategoride düzenlenmiştir:

* **Genel** -proje adını, açıklamasını ve varsayılan Namespace projenin konumunu yanı sıra, burada ayarlanan gibi bilgileri.
* **Derleme** -Bu, geliştiricilerin ayarlama veya taşınabilir sınıf kitaplıkları için PCL profillerini değiştirme olanak tanır. Ayrıca sağlar özel komutlar, yapılandırmaları, derleyici seçenekleri ayarlamak için. Çıkış yolu ve derleme adı da buradan ayarlanabilir.
* **Çalıştırma** -Bu, proje başına temelinde özel çalıştırma yapılandırmaları oluşturmanıza olanak sağlar.
* **Kaynak kodu** - Bu, birçok farklı dosya türleri biçimlendirme denetlemenize olanak tanır ve adlandırma kuralları. Ayrıca varsayılan üst bilgi stil ve adlandırma ilkeleri burada ayarlayabilirsiniz.
* **Sürüm denetimi** -bu sürüm denetimi projenizle kullanırken işleme iletisi stili düzenlemenizi sağlar.

Her proje, platforma bağlı olarak belirli proje seçenekleri içerebilir. Örneğin, aşağıdaki görüntüde gösterildiği gibi bir Xamarin.Android projesi Android için ilgili seçeneğe sahiptir (örneğin, bağlayıcı seçenekleri) derleme ve uygulamayı (örneğin, izinleri):

![Android projesi seçenekleri](media/projects-and-solutions-image5.png)

Xamarin.iOS paket grubu imzalama - gerekli sağlama profilinin gibi ilgili seçeneklerini içerir:

![iOS projesi seçenekleri](media/projects-and-solutions-image6.png)

## <a name="solution-options"></a>Çözüm seçenekleri

Çözüm seçenekleri gibi proje seçenekleri, ancak tüm çözümleri kapsamını kapsar. Derleme ayarları, kod stilleri ve sürüm denetimi, biçimlendirme, yazar bilgileri için bir yol sağlarlar ve başlangıç projesi çözümdeki atamak bir yol sağlar.  Çözüm Seçenekleri iletişim kutusunun yanından erişilebilen **Proje > çözüm seçenekleri** menü öğesi, gelen **seçenekleri** çözüm panelinde veya çift tıklatarak çözümdeki bağlam menüsü öğesi Çözümde, çözüm bölmesi:

![Çözüm seçenekleri](media/projects-and-solutions-image7.png)

## <a name="see-also"></a>Ayrıca bkz.

* [Proje ve çözüm özelliklerini (Windows için Visual Studio) yönetme](/visualstudio/ide/managing-project-and-solution-properties)