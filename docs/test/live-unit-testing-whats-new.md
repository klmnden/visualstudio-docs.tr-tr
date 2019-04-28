---
title: Live Unit Testing Visual Studio 2017'deki yenilikler
titleSuffix: ''
ms.date: 10/11/2017
ms.topic: conceptual
helpviewer_keywords:
- Live Unit Testing
- Live Unit Testing What's New
author: rpetrusha
ms.author: ronpet
ms.workload:
- dotnet
monikerRange: vs-2017
ms.openlocfilehash: 96ac53900806cc37e215342573f998be995289f8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62785890"
---
# <a name="whats-new-in-live-unit-testing-for-visual-studio-2017"></a>Live Unit Testing Visual Studio 2017'deki yenilikler

Bu konu Visual Studio 2017 sürüm 15.3 itibaren Visual Studio'nun her sürümü için Live Unit Testing eklenen yeni özellikleri listeler. Live Unit Testing kullanma genel bakış için bkz. [Visual Studio ile Live Unit Testing](live-unit-testing.md).

## <a name="version-154"></a>Sürüm 15.4

Visual Studio 2017 sürüm 15.4 ile başlayarak, Live Unit Testing iyileştirmeler ve geliştirmeler birtakım alanları içerir:

- **Geliştirilmiş bulunabilirliği**. Bilmiyorsanız kullanıcılar için Live Unit Testing özelliği yoksa, Visual Studio IDE kullanıcı birim testleri içeren bir çözümü açar ancak Live Unit Testing etkin olduğunda Live Unit Testing bahsetmeleri sarı renkte bir çubuk gösterir. Live Unit Testing hakkında daha fazla bilgi edinmek ve etkinleştirmek için kullanıcı gold çubuğunda görüntülenen bilgileri sağlar. Live Unit Testing Önkoşullar karşılanmadı olduğunda sarı renkli çubuk bilgi de görüntüler. Bu güncelleştirmeler şunlardır:

   - Test bağdaştırıcısı yok.
   - Eski test bağdaştırıcısı sürümleri yok.
   - Çözüm tarafından başvurulan NuGet paketlerini geri yüklemeye gereklidir.

- **Görev merkezi bildirimleri ile tümleştirme**. Visual Studio IDE artık kullanıcıların kolayca Live Unit Testing etkinleştirildiğinde neler anlatabilmeniz görev merkezi bildiriminde bir Live Unit Testing arka plan işlemleri gösterir. Bu anahtar üzerinde büyük bir çözümde Live Unit Testing başlangıç sorununu giderir. Kapsamı simgeleri göründüğü kadar daha önce birkaç dakika kullanıcılar olup Live Unit Testing gerçekten etkinleştirildi ve olup çalıştığı belirlenemedi. Artık değil!

- **MSTest framework sürüm 1 için destek**: Live Unit Testing zaten üç popüler birim test çerçeveleri ile çalışır: xUnit, NUnit ve MSTest. MSTest birim testi projelerini MS Test version 2 kullanıldığında daha önce Live Unit Testing yalnızca çalışıyordu. Visual Studio 2017 sürüm 15.4 ile başlayarak, şimdi de MSTest sürüm 1 de destekler.

- **Güvenilirlik ve performansa**: Live Unit Testing artık sistem projeleri tam yükleme tamamlamadıysanız daha iyi algılayabilir ve Live Unit Testing kilitlenen önler sağlar. Derleme performansı iyileştirmeleri ayrıca kaçının sistem projede hiçbir şey Dosya değişmiş olduğunu bilir, MSBuild projelerinin reevaluating.

- **Çeşitli kullanıcı arabirimi iyileştirmelerini**:  Kafa karıştırıcı **Canlı Test kümesi – Ekle/Çıkar** sağ tıklama hareketi seçeneğinden adlandırıldı **Live Unit Testing ekleme/çıkarma**. **Temiz sıfırlama** seçeneğini **Test** > **Live Unit Testing** menü kaldırıldı. Artık seçerek erişilebilir durumda **Araçları** > **seçenekleri** > **Live Unit Testing** seçerek **kalıcı verileri Sil** .

## <a name="version-153"></a>Sürüm 15.3

Visual Studio 2017 sürüm 15.3, Live Unit Testing özellikleri iyileştirmeler ve geliştirmeler iki önemli alanda başlangıç:

- .NET Core ve .NET Standard desteği. C# veya Visual Basic içinde yazılan .NET Core ve .NET Standard çözümler üzerinde Live Unit Testing ' ı kullanabilirsiniz.

- Performans geliştirmeleri. İlk tam derleme ve testleri Live Unit Testing altında çalıştırdıktan sonra performansı önemli ölçüde daha hızlı olduğunu fark edeceksiniz. Ayrıca, önemli bir performans geliştirmesi sonraki başlangıçlarda Live Unit Testing, aynı çözümdeki görürsünüz. Biz artık Live Unit Testing tarafından oluşturulan verileri kalıcı hale getirmek ve güncel denetimleri ile mümkün olduğunca yeniden.

Bu önemli eklemeler yanı sıra, Live Unit Testing, aşağıdaki geliştirmeleri içerir:

- Yeni beaker simgesi artık bir test yöntemi, normal yöntemlerinden ayırt etmek için kullanılır. Live Unit Testing özel test dahil edilmeyen boş beaker simge belirtir.

- Kullanıcı Arabirimi pencere Live Unit Testing kapsamı simgesinin bir test metodu tıklayarak, artık UI penceresinde ve kod düzenleyicisinden çıkmak zorunda kalmadan bu bağlamı testinden doğru hata ayıklama seçeneği var. Bu, özellikle başarısız bir test sırasında ararken kullanışlıdır.

- Araçlar/Seçenekler/Live Unit Testing / genel birkaç ek yapılandırılabilir seçeneklerin eklenmiştir. Live Unit Testing için kullanılan bellek sınırı uygularız. Açık çözümünüz için Live Unit Testing kalıcı verileri için dosya yolunu da belirtebilirsiniz.

- Menü çubuğunda, Test/Live Unit Testing altında birkaç ek menü öğeleri eklendi. **Temiz sıfırlama** kalıcı verilerini siler ve yeniden oluşturur. **Seçenek** Araçlar/Seçenekler/Live Unit Testing / genel atlar.

- Kaynak kodunda hedeflenen test yöntemleri Live Unit Testing hariç tutmak istediğinizi belirtmek için artık şu öznitelikleri kullanabilirsiniz:

   - XUnit için: `[Trait("Category", "SkipWhenLiveUnitTesting")]`
   - NUnit için: `[Category("SkipWhenLiveUnitTesting")]`
   - MSTest için: `[TestCategory("SkipWhenLiveUnitTesting")]`

## <a name="see-also"></a>Ayrıca bkz.

- [Dinamik Birim Testine Giriş](live-unit-testing-intro.md)
- [Visual Studio ile Live Unit Testing](live-unit-testing.md)
