---
title: Kod haritaları yavaş çalışıyor
ms.date: 05/16/2018
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 12ba03ab97da3295a93b54dfc012d10fc012fd30
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62423935"
---
# <a name="improve-performance-for-code-maps"></a>Kod haritaları için performansı

İlk kez bir eşleme oluşturduğunuzda, Visual Studio bulduğu tüm bağımlılıkların dizinini oluşturur. Bu işlem, özellikle büyük çözümler için biraz zaman alabilir ancak sonraki performansını artırır. Kod değişirse, Visual Studio yalnızca güncelleştirilmiş kod reindexes. Harita işleme tamamlamak geçen süreyi en aza indirmek için aşağıdaki önerileri göz önünde bulundurun:

- İlginizi çeken bağımlılıkların eşleyin.

- Çözümün tamamı için harita oluşturmadan önce çözüm kapsamını azaltın.

- Seçerek otomatik yapı çözümü kapatmak **Atla derleme** kod harita araç çubuğunda.

- Otomatik üst öğelerinin seçerek ekleme devre dışı kapatma **dahil üst** kod harita araç çubuğunda.

   ![Derleme ve üst öğeleri dahil düğmeleri atla](../modeling/media/codemapsfilterskipbuildicons.png)

- Düğümlere ve bağlantılara ihtiyacınız olmayan doğrudan kaldırmak için kod Haritası dosyasını düzenleyin. Haritanın değiştirilmesi, arka plandaki kod etkilemez. Bkz: [DGML dosyalarını düzenleyerek kod haritalarını özelleştirme](../modeling/customize-code-maps-by-editing-the-dgml-files.md).

Eşlemeleri oluşturmak veya bir eşlemden öğeleri eklemek için daha uzun sürebilir **Çözüm Gezgini** bir proje öğesi ayarlandığında **çıkış dizinine Kopyala** özelliği **her zaman Kopyala**. Performansı artırmak için bu özelliği değiştirmek **yeniyse Kopyala** veya `PreserveNewest`. Bkz: [artımlı derlemeleri](../msbuild/incremental-builds.md).

Tamamlanan harita yalnızca başarıyla oluşturulmuş kod için bağımlılıkları gösterir. Derleme hataları belirli bileşenleri meydana gelirse, bu hatalar harita üzerinde görüntülenir. Bir bileşenin gerçekten oluştuğundan ve harita üzerinde temel mimari kararlar almadan önce bağımlılıkları olduğundan emin olun.