---
title: JavaScript
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-javascript
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: f3eee13e-30e4-4bc1-81f5-058d7e379b75
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: bcd092ca1631f54f758cef95895d8509d14dec96
ms.sourcegitcommit: f6dd17b0864419083d0a1bf54910023045526437
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/27/2018
ms.locfileid: "53802984"
---
# <a name="javascript-in-visual-studio"></a>Visual Studio’da JavaScript
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

JavaScript, Visual Studio'da birinci sınıf bir dildir. Visual Studio IDE'de JavaScript kodu yazarken standart düzenleme yardımlarının (kod parçacıkları, IntelliSense, vb.) çoğunu veya tümünü kullanabilirsiniz. Birçok uygulama türleri ve hizmetler için JavaScript kodu yazabilirsiniz.

 JavaScript dili referans belgeleri için bkz. [JavaScript](http://msdn.microsoft.com/library/d1et7k7c\(v=vs.94\).aspx).

 Belirli uygulama türlerini ve HTML ve JavaScript kullanarak hizmetleri geliştirmek için Visual Studio ya da belirli Visual Studio uzantıları belirli sürümlerini gerekebilir. Aşağıdaki listede, daha fazla bilgi için bağlantılar içerir.

- Apache Cordova kullanarak platformlar arası uygulamalar oluşturmak için [Apache Cordova için Visual Studio Araçları edinin](http://go.microsoft.com/fwlink/p/?LinkId=397606).

- Oluşturulacak [Windows Store](http://dev.windows.com/develop), [Windows Phone](http://dev.windows.com/develop)hem de Evrensel uygulamalar (her iki platform destekleyen) [araçları edinin](http://dev.windows.com/en-us/develop/downloads).

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
|Gösterir|[Öneriler](/visualstudio/scripting-docs/javascript/reference/promise-object-javascript) daha kolay ve Temizleyicisi zaman uyumsuz kodlama izin verin. Promise oluşturucular desteklenir, bunların ile `all` ve `race` yardımcı program yöntemleri.|
|Yineleyiciler|Artık her ayrı bir özellik değeri için çalıştırılacak deyimleri ile bir özel yineleme kancası çağırma (diziler, dizi benzeri nesneleri ve yineleyiciler dahil) iterable nesneler üzerinde yineleyebilirsiniz. Daha fazla bilgi için [yineleyiciler ve oluşturucular](/visualstudio/scripting-docs/javascript/advanced/iterators-and-generators-javascript). **Not:**  Oluşturucuları henüz desteklenmemektedir.|
|Ok işlevleri|Ok işlevinde (= >) için toplu değer sözdizimi sağlar `function` bir sözcük özellikleri anahtar sözcüğünü `this` bağlama.|
|Yerleşik nesneler için yeni yöntemler|[Dizi nesnesi](/visualstudio/scripting-docs/javascript/reference/array-object-javascript), [matematik nesnesi](/visualstudio/scripting-docs/javascript/reference/math-object-javascript), [sayı nesne](/visualstudio/scripting-docs/javascript/reference/number-object-javascript), [nesne nesnesi](/visualstudio/scripting-docs/javascript/reference/object-object-javascript), ve [dize nesnesi](/visualstudio/scripting-docs/javascript/reference/string-object-javascript) yerleşik nesneler, birçok yeni yardımcı işlevleri ve verileri inceleme ve düzenleme için özellikleri içerir.|
|Nesne sabit değeri geliştirmeleri|Nesneler artık hesaplanan özellikler, kısa yöntemi tanımları ve toplu değer sözdizimi değeri için aynı adlı bir değişken başlatılır özellikleri destekler. Daha fazla bilgi için [nesneleri oluşturma](/visualstudio/scripting-docs/javascript/creating-objects-javascript).|
|Proxy'ler|[Proxy'leri](/visualstudio/scripting-docs/javascript/reference/proxy-object-javascript) özel davranış nesneler için etkinleştirin.|
|REST parametreleri|REST parametreler ardışık bağımsız değişken bir dizi işlev çağrısında olanak sağlar. Daha fazla bilgi için [işlevleri](/visualstudio/scripting-docs/javascript/functions-javascript).|
|Spread işleci|[Yayılma işleci](/visualstudio/scripting-docs/javascript/reference/spread-operator-decrement-dot-dot-dot-javascript) (`…`) bağımsız iterable ifadelere genişletir. Örneğin, `a.b(…array)` yaklaşık olarak aynı olduğundan `a.b.apply(a, array)`.|
|Simgeleri|[Sembol](/visualstudio/scripting-docs/javascript/reference/symbol-object-javascript) nesneler girişim varolan nesne özellikleri, hiçbir istenmeyen görünürlük ve diğer eşgüdümlü olmayan eklemeler kaybetme riski varolan nesnelerle başka kod tarafından eklenecek özellikleri sağlar.|
|Şablon dizeleri|[Şablon dizeleri](/visualstudio/scripting-docs/javascript/advanced/template-strings-javascript) ifadeler değerlendirilir ve bitişik dize sabit değeri izin dize sabitleri sabit değerlerdir.|
|Unicode geliştirmeleri|Geliştirmeler yapılmıştır Unicode desteği. Örneğin, yeni bir kaçış dizisi biçimi astral kod noktası (dörtten fazla onaltılı basamaklar içeren kod noktaları) destekler. Daha fazla bilgi için [özel karakterler](/visualstudio/scripting-docs/javascript/advanced/special-characters-javascript).|
|WeakSet|A [WeakSet](/visualstudio/scripting-docs/javascript/reference/weakset-object-javascript) olan başka bir yerde başvurulan değillerse atık olacak nesneleri koleksiyonu.|
