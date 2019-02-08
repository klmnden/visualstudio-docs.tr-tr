---
title: Kod Parçacıkları
description: Mac için Visual Studio'da verimli bir şekilde programlanacağı kod parçacıkları kullanma
author: conceptdev
ms.author: crdun
ms.date: 02/07/2019
ms.assetid: 0FE27C0C-A861-4133-A74E-8D0505CF5342
ms.openlocfilehash: 56f736aa1e32530b1db96ad301091151731b7d28
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55921256"
---
# <a name="code-snippets"></a>Kod parçacıkları

Kod parçacıkları, genellikle olarak adlandırılan _kod şablonları_önceden yazılmış kod bloklarını düzenleme ve bunlar eklemeye izin verecek şekilde etkili programlama için kullanışlıdır. Yeni desenler, geliştirici olarak da öğrenmeye yönelik da sözdizimi emin değilseniz veya kod parçacıkları ortak desenler hızlı bir şekilde eklemek için kullanışlı olabilir. Şablonlar için sağlanan C#, F#, HTML, XML, Python ve Razor.

Bu bölümde, oluşturma, ekleme ve kod parçacıklarını kullanma açıklanmaktadır.

## <a name="inserting-a-snippet"></a>Bir kod parçacığı ekleme

Kod parçacıkları, bunlardan bazıları aşağıda açıklanmıştır eklemek için bazı farklı yolu vardır:

- **Sekme genişletmeyi** &ndash; şablon adını yazmaya başlayın, liste ve ENTER tuşuna seçin **sekmesini**, **sekmesini** eklemek için:

  ![Sekme genişletmeyi kod](media/source-editor-image13.png)

- **Araç kutusu** &ndash; tüm kod parçacıkları listesini görüntülemek için araç takımını kullanın. Herhangi bir şablon kaynak kodu doğru konumda araç kutusundan sürükleyin:

  [![Araç kutusu kod parçacıkları](media/source-editor-image14-sml.png)](media/source-editor-image14.png#lightbox)

- **Şablonları komut Ekle** &ndash; şu anda bir şablon eklemek için set bağlama varsayılan anahtarı yok. Oluşturmak için Gözat **Visual Studio > Tercihler > anahtar bağlamaları** araması `template`. Bu bağlama düzen alanına istenen anahtar bağlaması ekleniyor sağlar, ardından **Uygula**:

  ![İç Metin şablonu komutu](media/source-editor-image15.png)

## <a name="creating-a-new-template"></a>Yeni şablon oluşturma

Birçok var olan şablonu kullanın ve düzenleme dilleri çeşitli olsa da, yeni şablonlar da giderek eklenebilir **Visual Studio > Tercihler > Metin Düzenleyicisi > kod parçacıkları**:

![Yeni şablon iç](media/source-editor-image12.png)

Tuşuna **Ekle** veya **Düzenle** oluşturma veya düzenleme kod parçacıklarını düğmeleri.

## <a name="keywords-in-code-snippets"></a>Kod parçacığı anahtar sözcükleri

Düzenleyiciye bir kod parçacığı eklendikten sonra tanımlanan herhangi bir anahtar sözcük vurgulanır ve bunlar arasında sekmeyle gitmeyi düzenlenebilir. Anahtar sözcükler, kod parçacığında bir "değişken" gibi davranır ve bir dolar işareti koyarak tanımlanan `$` anahtar adından önce ve sonra. 

**Şablonu Düzen** penceresini aşağıda gösterilmektedir, yerleşik düzenleme `prop` kod parçacığı. İki anahtar sözcüğü kod parçacığının içerdiği &ndash; `$type$` ve `$name$` &ndash; olabilen ek özelliklerini (varsayılan değer ve araç ipucu gibi), pencerenin sağ tarafında ayarla:

![Şablon pencere Düzenle](media/source-editor-image12z.png)

Aşağıdaki alanlar, bir kod parçacığı tanımlamak için kullanılır:

- **Kısayol** &ndash; metin kod parçacığını eklemek için kullanıcı türleri.
- **Grup** &ndash; parçacıkları arada gruplandırılır kod parçacığı içerik menüsünü kullanarak bu değeri.
- **Açıklama** &ndash; parçacığının amaçlı açıklaması.
- **MIME** &ndash; hangi dosya türleri kod parçacığı kullanılabilir denetler.
- **Genişletilebilir şablonu** &ndash; kısayol tuşlarına basarak imleci kod parçacığı eklenebilir böylece seçili emin olun.
- **Şablon çevrelemeyi olduğu** &ndash; bu kısayol, listelemek için bu seçeneği işaretleyin **Şununla Çevrele...**  Düzenleyicisi'nde içerik menüsü.
- **Şablon metni** &ndash; gerçek kod parçacığı düzenleyicide yerleşik eklenir. Anahtar sözcük yer tutucuları, dolar işareti belirteciyle örn çevreleyen tarafından tanımlanabilir. `$type$`.
- **Anahtar özellik paneli** &ndash; bir anahtar sözcük seçmek için sağ tarafında penceresinin, açılır listede üstündeki kullanın (örn `type`) ve varsayılan değer ve araç ipucu gibi özelliklerini düzenleyin.

## <a name="using-keywords-in-the-editor"></a>Anahtar sözcükler Düzenleyicisi'nde kullanma

Yukarıda bir tanımlandığı gibi bir kod parçacığı anahtar sözcükleri ile kullanmak için tuşuna basın ve kısayol yazın **sekmesini** iki kez ve kod parçacığı içeriği imlecin eklenir:

![Eklenen kod parçacığı anahtar sözcükleri gösteriliyor](media/source-editor-image12a.png)

Tuşuna **sekmesini** arasında taşımak için anahtar `object` ve `MyProperty` sınıfınız için kod parçacığı özelleştirmek için.

Bunun gibi bir kod parçacığı, bir anahtar sözcük yinelenebilir `for` örnek, bildirim `$i$` anahtar sözcüğü 3 kez görüntülenir:

![Yinelenen anahtar sözcüklerle parçacık şablonu](media/source-editor-image12b.png)

Düzenleyici'de kullanıldığında **sekmesini** anahtar ilk arasında geçirir `i` ve `max`. Varsa, üzerine yazma `i` üç hepsinin farklı bir değişken adı ile güncelleştirilir:

![Birden çok anahtar sözcükleri gösteren eklenen kod parçacığı](media/source-editor-image12c.png)

### <a name="reserved-keywords"></a>ayrılmış anahtar sözcükler

Bir kod parçacığında kullanabileceğiniz iki ayrılmış anahtar sözcükler vardır:

- `$selected$` &ndash; Kod parçacığı varsa **şablon çevrelemeyi olan** işaretli bu anahtar sözcük kod parçacığı seçildi, düzenleyicide vurgulanan metin tarafından değiştirilir.
- `$end$` &ndash; İmleç bir kod parçacığı anahtar sözcükleri düzenleme kullanıcı sona erdiğinde konumunda yerleştirilecek `$end$` anahtar sözcüğü.

`for` Kod parçacığı önceki bölümde hem bu ayrılmış anahtar sözcükler örneğidir.

Başvurmak [Visual Studio kod parçacıkları başvurusu](/visualstudio/ide/code-snippets-schema-reference#keywords) daha fazla bilgi için.

## <a name="see-also"></a>Ayrıca bkz.

- [Kod parçacıkları (Windows için Visual Studio)](/visualstudio/ide/code-snippets)