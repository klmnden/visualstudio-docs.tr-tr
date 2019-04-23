---
title: Arapça ve İbranice uygulamaları desteği
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- Hebrew character display, creating applications
- bidirectional language support, about bidirectional language support
- Arabic language, creating applications
ms.assetid: b56f9795-ed8d-4452-9d49-8ca0b0145d86
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d09ad8644c30be76c38cf4b819d09ee1c470cb39
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60048185"
---
# <a name="create-applications-in-bidirectional-languages"></a>Çift yönlü dillerde uygulamalar oluşturma

Sağ-Arapça ve İbranice gibi sola doğru dillerde yazılan metin görüntüleyen uygulamalar oluşturmak için Visual Studio kullanabilirsiniz. Bazı özellikler için özellikleri ayarlayabilirsiniz. Diğer durumlarda, kod özellikleri uygulamalıdır.

> [!NOTE]
> Girin ve çift yönlü diller görüntülemek için uygun dili ile yapılandırılmış bir Windows sürümü ile çalışmalısınız. Bu bir İngilizce sürümüyle ilgili dil paketi yüklü olan Windows veya Windows uygun şekilde yerelleştirilmiş sürümünü olabilir.

## <a name="types-of-applications-that-support-bidirectional-languages"></a>Çift yönlü dil desteği uygulama türleri

- Windows uygulamaları

   Tam olarak iki yönlü metnin sağdan sola okuma düzeni ve yansıtma (windows, menüler, iletişim kutuları ve benzeri düzenini ters) için destek içeren çift yönlü uygulamalar oluşturabilirsiniz. Yansıtma dışında bu özellikler varsayılan olarak veya özellik ayarları olarak kullanılabilir. Yansıtma ileti kutuları gibi bazı özellikler için doğal olarak desteklenir. Ancak, diğer durumlarda kod yansıtma uygulamalıdır. Daha fazla bilgi için [Windows Forms uygulamaları için çift yönlü destek](/dotnet/framework/winforms/advanced/bi-directional-support-for-windows-forms-applications).

- Web uygulamaları

   Web Hizmetleri, UTF-8 ve çift yönlü diller gerektiren uygulamalar için uygun hale getirir, Unicode metni gönderip destekler. Web istemcisi uygulamalarını tarayıcılar için kullanıcı arabirimini kullanır, çift yönlü derecesini, destek için bir web uygulaması kullanıcı tarayıcısı bu çift yönlü Özellikler ne kadar iyi destekleyen bağlıdır. Visual Studio'da, Arapça veya İbranice metin, sağdan sola okuma düzeni, dosya kodlamasını ve yerel kültür ayarları için desteğe sahip uygulamalar oluşturabilirsiniz. Daha fazla bilgi için [ASP.NET web uygulamaları için çift yönlü destek](https://msdn.microsoft.com/Library/5576f9b1-9b86-41ef-8354-092d366bcd03).

Konsol uygulamaları, metin çift yönlü dil desteği içermez. Windows konsol uygulamaları ile nasıl çalıştığına ilişkin bir sonucu budur.

## <a name="fully-supported-features"></a>Tam olarak desteklenen özellikler

Visual Studio'da tasarım zamanında çift yönlü diller aşağıdaki şekillerde kullanabilirsiniz:

- **Metin girişi**

   Visual Studio Unicode'u destekler, dolayısıyla sisteminizi ayarlanmış uygun yerel ve giriş dili, Arapça veya İbranice metin girebilirsiniz. (Keşide ve aksan Arapça desteği içerir.)

- **Nesne adları**

   Çift yönlü diller çözümleri, projeleri, dosyaları, klasörleri ve benzeri için ad atamak için kullanabilirsiniz. Kodu, değişkenleri, sınıflar, nesne, öznitelikler, meta verileri ve diğer öğeleri adları için çift yönlü diller kullanabilirsiniz.

- **Dosya kodlama**

   Kaydet ve dosyaları bir dile özgü veya Unicode kodlaması ile açın. Daha fazla bilgi için [nasıl yapılır: Kaydetme ve açma dosyaları kodlamayla](../ide/how-to-save-and-open-files-with-encoding.md).

## <a name="features-with-limited-support"></a>Özellikleri desteği

### <a name="right-to-left-reading-order"></a>Sağdan sola okuma düzeni

Varsayılan olarak, Visual Studio'daki metin girişi denetimleri sağdan sola okuma düzeni kullanın. Çoğu durumda, standart Windows hareketleri okuma sırasını değiştirmek için kullanabilirsiniz. Örneğin, basabilirsiniz **Ctrl**+**RightShift** geçiş yapmak için **özellikleri** özellik değerleri için sağdan sola okuma düzeni desteklemek için penceresi. Ancak, sağdan sola okuma düzeni, Visual Studio'da her yerde desteklenmez:

- Her zaman onay kutuları, açılan listeler ve diğer Visual Studio iletişim kutularındaki denetimler sağdan sola okuma düzeni kullanın.

- Kod Düzenleyicisi'ni (ve metin düzenleyici) sağdan sola okuma düzeni desteklemez. Bir çift yönlü dil metin girebilirsiniz, ancak okuma her zaman sol ve sağ sırasıdır.

## <a name="arabic-or-hebrew-object-names"></a>Arapça veya İbranice nesne adları

Arapça veya İbranice metin, klasörleri, değişkenleri veya diğer nesnelerin adları atamak için kullanabilirsiniz. Arapça ile çalışırken Keşide ve aksan işaretleri dahil olmak üzere herhangi bir Arapça karakter kullanabilirsiniz.

Aşağıdaki öğeleri, Arapça veya İbranice kullanarak adlı ve Visual Studio doğru şekilde işlenir:

- Çözüm, proje ve proje yola dahil tüm klasörleri dahil olmak üzere, dosya adları. **Çözüm Gezgini** doğru çözüm ve öğe adlarını görüntüler.

- Dosya içerikleri. Açabilir veya dosyaları Unicode kodlama veya seçili bir kod sayfası ile kaydedin.

    > [!NOTE]
    > Kod Düzenleyicisi, sağdan sola okuma düzeni desteklemez.

- Veri öğeleri. **Sunucu Gezgini** bu öğeleri doğru görüntüler ve bunları düzenlemenize olanak sağlar.

- Öğeleri Windows panoya kopyalandı.

- Öznitelikler ve meta verileri.

- Özellik değeri. Arapça veya İbranice metin kullanabileceğiniz **özellikleri** penceresi. Pencere, standart Windows tuş vuruşları kullanarak sağdan sola ve sağa sola okuma düzeni arasında geçiş yapmanıza izin verir (**Ctrl**+**RightShift** sağdan sola ve **Ctrl**+**LeftShift** soldan sağa için).

- Kod ve metin. Kod Düzenleyicisi'nde, Arapça veya İbranice adı sınıfları, İşlevler, değişkenleri, özellikleri, dize değişmez değerleri, öznitelikleri ve benzeri için kullanabilirsiniz. Ancak, düzenleyici sağdan sola okuma düzeni desteklemez; metin her zaman sol kenar boşluğunda başlatır.

    > [!TIP]
    > Bunları, programlarına kodlamak yerine kaynak dosyalarında dize değişmez değerleri yerleştirmeniz gerekir. Daha fazla bilgi için [(.NET Framework) masaüstü uygulamalarında kaynakların](/dotnet/framework/resources/index).

    > [!NOTE]
    > Nasıl, Arapça ve İbranice adlı nesnelere başvurmak için tutarlı olması gerekir. Arapça bir değişkeni adlandırmada Kaşida kullanırsanız, örneğin, her zaman Kaşida söz konusu olduğunda değişken veya hataları neden olur kullanmanız gerekir.

- Kod açıklamaları. Açıklamalar, Arapça veya İbranice oluşturabilirsiniz. Açıklama Oluşturucu aracında bu diller de kullanabilirsiniz.