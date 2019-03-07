---
title: JavaScript
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-javascript
ms.topic: conceptual
ms.assetid: f3eee13e-30e4-4bc1-81f5-058d7e379b75
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 66132724b5ece0570ead7c12949dfc5650521b29
ms.sourcegitcommit: b7f25ae08e45fcaa84a84276b588cf6799cc7620
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/07/2019
ms.locfileid: "57567389"
---
# <a name="javascript-in-visual-studio"></a>Visual Studio’da JavaScript
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

JavaScript, Visual Studio'da birinci sınıf bir dildir. Visual Studio IDE'de JavaScript kodu yazarken standart düzenleme yardımlarının (kod parçacıkları, IntelliSense, vb.) çoğunu veya tümünü kullanabilirsiniz. Birçok uygulama türleri ve hizmetler için JavaScript kodu yazabilirsiniz.

 JavaScript dili referans belgeleri için bkz. [JavaScript](http://msdn.microsoft.com/library/d1et7k7c\(v=vs.94\).aspx).

 Belirli uygulama türlerini ve HTML ve JavaScript kullanarak hizmetleri geliştirmek için Visual Studio ya da belirli Visual Studio uzantıları belirli sürümlerini gerekebilir. Aşağıdaki listede, daha fazla bilgi için bağlantılar içerir.

- Apache Cordova kullanarak platformlar arası uygulamalar oluşturmak için [Apache Cordova için Visual Studio Araçları edinin](http://go.microsoft.com/fwlink/p/?LinkId=397606).

- Oluşturulacak [Windows Store](http://dev.windows.com/develop), [Windows Phone](http://dev.windows.com/develop)hem de Evrensel uygulamalar (her iki platform destekleyen) [araçları edinin](https://developer.microsoft.com/windows/downloads).

- Bulut tabanlı hizmetler oluşturmak için bkz [Microsoft Azure sitesine](http://azure.microsoft.com/documentation/).

- Web siteleri ve web uygulamaları oluşturmak için [ASP.NET sitesine](http://www.asp.net/get-started/websites).

  > [!NOTE]
  >  Boş bir ASP.Net Web sitesi oluşturabileceğinizi ve HTML, CSS ve JavaScript programlama için kullanın. Visual Studio'da hata ayıklama ASP.NET tarafından sağlanan Webconfig dosyası etkinleştirir (veya uygulamayı çalıştırdığınızda F12 araçları da kullanabilirsiniz).

  Visual Studio'daki JavaScript düzenleyicisi IntelliSense desteği sunar. Daha fazla bilgi için bkz. [JavaScript IntelliSense](../ide/javascript-intellisense.md).

## <a name="whats-new-in-javascript"></a>Javascript'teki Yenilikler
 Yeni JavaScript özellikleri, aşağıdaki tabloda listelenmiştir.

|Özellik|Açıklama|
|-------------|-----------------|
|Sınıflar|Yeni sözdizimi bildirimini destekler [sınıfları](/visualstudio/scripting-docs/javascript/reference/class-statement-javascript).|
|Gösterir|[Öneriler](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise) daha kolay ve Temizleyicisi zaman uyumsuz kodlama izin verin. Promise oluşturucular desteklenir, bunların ile `all` ve `race` yardımcı program yöntemleri.|
|Yineleyiciler|Artık her ayrı bir özellik değeri için çalıştırılacak deyimleri ile bir özel yineleme kancası çağırma (diziler, dizi benzeri nesneleri ve yineleyiciler dahil) iterable nesneler üzerinde yineleyebilirsiniz. Daha fazla bilgi için [yineleyiciler ve oluşturucular](/visualstudio/scripting-docs/javascript/advanced/iterators-and-generators-javascript). **Not:**  Oluşturucuları henüz desteklenmemektedir.|
|Ok işlevleri|Ok işlevinde (= >) için toplu değer sözdizimi sağlar `function` bir sözcük özellikleri anahtar sözcüğünü `this` bağlama.|
|Yerleşik nesneler için yeni yöntemler|[Dizi nesnesi](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array), [matematik nesnesi](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math), [sayı nesne](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number), [nesne nesnesi](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object), ve [dize nesnesi](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String) yerleşik nesneler, birçok yeni yardımcı işlevleri ve verileri inceleme ve düzenleme için özellikleri içerir.|
|Nesne sabit değeri geliştirmeleri|Nesneler artık hesaplanan özellikler, kısa yöntemi tanımları ve toplu değer sözdizimi değeri için aynı adlı bir değişken başlatılır özellikleri destekler. Daha fazla bilgi için [nesneleri oluşturma](/visualstudio/scripting-docs/javascript/creating-objects-javascript).|
|Proxy'ler|[Proxy'leri](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy) özel davranış nesneler için etkinleştirin.|
|REST parametreleri|REST parametreler ardışık bağımsız değişken bir dizi işlev çağrısında olanak sağlar. Daha fazla bilgi için [işlevleri](/visualstudio/scripting-docs/javascript/functions-javascript).|
|Spread işleci|[Yayılma işleci](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Spread_operator) (`…`) bağımsız iterable ifadelere genişletir. Örneğin, `a.b(…array)` yaklaşık olarak aynı olduğundan `a.b.apply(a, array)`.|
|Simgeleri|[Sembol](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Symbol) nesneler girişim varolan nesne özellikleri, hiçbir istenmeyen görünürlük ve diğer eşgüdümlü olmayan eklemeler kaybetme riski varolan nesnelerle başka kod tarafından eklenecek özellikleri sağlar.|
|Şablon dizeleri|[Şablon dizeleri](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Template_literals) ifadeler değerlendirilir ve bitişik dize sabit değeri izin dize sabitleri sabit değerlerdir.|
|Unicode geliştirmeleri|Geliştirmeler yapılmıştır Unicode desteği. Örneğin, yeni bir kaçış dizisi biçimi astral kod noktası (dörtten fazla onaltılı basamaklar içeren kod noktaları) destekler. Daha fazla bilgi için [özel karakterler](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions#Types_of_special_characters).|
|WeakSet|A [WeakSet](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/WeakSet) olan başka bir yerde başvurulan değillerse atık olacak nesneleri koleksiyonu.|
