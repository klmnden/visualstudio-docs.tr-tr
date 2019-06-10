---
title: Arapça ve İbranice desteği
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- Hebrew character display [Visual Studio]
- bidirectional language support
- Arabic, creating applications
ms.assetid: b56f9795-ed8d-4452-9d49-8ca0b0145d86
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1271e5160920dc79decc9acc98aa1e5e3d936ca5
ms.sourcegitcommit: 51dad3e11d7580567673e0d426ab3b0a17584319
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/10/2019
ms.locfileid: "66823564"
---
# <a name="support-for-bidirectional-languages-in-visual-studio"></a>Visual Studio'da çift yönlü dil desteği

Visual Studio, Arapça ve İbranice metin doğru görüntüleyebilir ve nesne adları ve değerleri için çift yönlü metin girmenize olanak tanır.

> [!NOTE]
> Girin ve çift yönlü diller görüntülemek için uygun dili ile yapılandırılmış bir Windows sürümü ile çalışmalısınız. Bu bir İngilizce sürümüyle ilgili dil paketi yüklü olan Windows veya Windows uygun şekilde yerelleştirilmiş sürümünü olabilir.

## <a name="fully-supported-features"></a>Tam olarak desteklenen özellikler

Visual Studio'da tasarım zamanında çift yönlü diller, adlandırma, metin girme ve kaydetme ve dosya açma kullanabilirsiniz.

### <a name="text-entry"></a>Metin girişi

Visual Studio Unicode'u destekler, dolayısıyla sisteminizi ayarlanmış uygun yerel ve giriş dili, Arapça veya İbranice metin girebilirsiniz. (Keşide ve aksan Arapça desteği içerir.)

### <a name="arabic-or-hebrew-object-names"></a>Arapça veya İbranice nesne adları

Çift yönlü diller çözümleri, projeleri, dosyaları, klasörleri ve benzeri için ad atamak için kullanabilirsiniz. Kodu, değişkenleri, sınıflar, nesne, öznitelikler, meta verileri ve diğer öğeleri adları için çift yönlü diller kullanabilirsiniz. Arapça ile çalışırken Keşide ve aksan işaretleri dahil olmak üzere herhangi bir Arapça karakter kullanabilirsiniz.

Aşağıdaki öğeleri, Arapça veya İbranice kullanarak adlı ve Visual Studio tarafından doğru şekilde işlenir:

- Çözüm, proje ve proje yola dahil tüm klasörleri dahil olmak üzere, dosya adları.

   **Çözüm Gezgini** doğru çözüm ve öğe adlarını görüntüler.

- Dosya içerikleri.

   Açabilir veya dosyaları Unicode kodlama veya seçili bir kod sayfası ile kaydedin.

- Veri öğeleri.

   **Sunucu Gezgini** bu öğeleri doğru görüntüler ve bunları düzenleyebilirsiniz.

- Öğeleri Windows panoya kopyalandı.

- Öznitelikler ve meta verileri.

- Özellik değeri.

   Arapça veya İbranice metin kullanabileceğiniz **özellikleri** penceresi. Pencere, standart Windows tuş vuruşları kullanarak sağdan sola ve sağa sola okuma düzeni arasında geçiş yapmanıza izin verir (**Ctrl**+**RightShift** sağdan sola ve **Ctrl**+**LeftShift** soldan sağa için).

- Kod ve metin.

   Kod Düzenleyicisi'nde, Arapça veya İbranice adı sınıfları, İşlevler, değişkenleri, özellikleri, dize değişmez değerleri, öznitelikleri ve benzeri için kullanabilirsiniz. Ancak, düzenleyici sağdan sola okuma düzeni desteklemez; metin her zaman sol kenar boşluğunda başlatır.

   > [!TIP]
   > Bunları, programlarına kodlamak yerine kaynak dosyalarında dize değişmez değerleri yerleştirmeniz gerekir. Daha fazla bilgi için [(.NET Framework) masaüstü uygulamalarında kaynakların](/dotnet/framework/resources/index).

   > [!NOTE]
   > Nasıl, Arapça ve İbranice adlı nesnelere başvurmak için tutarlı olması gerekir. Arapça bir değişkeni adlandırmada Kaşida kullanırsanız, örneğin, her zaman Kaşida söz konusu olduğunda değişken veya hataları neden olur kullanmanız gerekir.

- Kod açıklamaları. Açıklamalar, Arapça veya İbranice oluşturabilirsiniz. Açıklama Oluşturucu aracında bu diller de kullanabilirsiniz.

### <a name="file-encoding"></a>Dosya kodlama

Kaydet ve dosyaları bir dile özgü veya Unicode kodlaması ile açın. Daha fazla bilgi için [nasıl yapılır: Kaydetme ve açma dosyaları kodlamayla](../ide/how-to-save-and-open-files-with-encoding.md).

## <a name="right-to-left-reading-order"></a>Sağdan sola okuma düzeni

Visual Studio, sağdan sola okuma düzeni için destek sınırlıdır. Varsayılan olarak, Visual Studio'daki metin girişi denetimleri sağdan sola okuma düzeni kullanın. Çoğu durumda, standart Windows hareketleri okuma sırasını değiştirmek için kullanabilirsiniz. Örneğin, basabilirsiniz **Ctrl**+**RightShift** geçiş yapmak için **özellikleri** özellik değerleri için sağdan sola okuma düzeni desteklemek için penceresi.

Sağdan sola okuma düzeni, Visual Studio aşağıdaki bölümlerinde desteklenmez:

- Her zaman onay kutuları, açılan listeler ve diğer Visual Studio iletişim kutularındaki denetimler sağdan sola okuma düzeni kullanın.

- Kod Düzenleyicisi'ni (ve metin düzenleyici) sağdan sola okuma düzeni desteklemez. Bir çift yönlü dil metin girebilirsiniz, ancak okuma her zaman sol ve sağ sırasıdır.

## <a name="see-also"></a>Ayrıca bkz.

- [Genelleştirilmiş ve yerelleştirilmiş uygulamalar geliştirin](globalizing-and-localizing-applications.md)
