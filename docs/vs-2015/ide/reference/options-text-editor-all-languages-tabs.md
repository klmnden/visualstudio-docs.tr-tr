---
title: Seçenekler, metin düzenleyici, tüm diller, sekmeler | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.ResJSON.Tabs
- VS.ToolsOptionsPages.Text_Editor.JavaScript.Tabs
- VS.ToolsOptionsPages.Text_Editor.All_Languages.Tabs
helpviewer_keywords:
- indents, Code Editor
- Code Editor, default behavior
- tabs, setting in Code Editor
- All Languages Text Editor Options dialog box
- editors, Code Editor
- Code Editor, indenting
- Code Editor, tabs
ms.assetid: 7e208e1d-5e3a-4bf7-a27b-4417e3e049c7
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: c89154cef2325da8b8073ded264afeb8f765302a
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54800810"
---
# <a name="options-text-editor-all-languages-tabs"></a>Seçenekler, Metin Düzenleyici, Tüm Diller, Sekmeler
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Bu iletişim kutusu Kod Düzenleyicisi'nin varsayılan davranışını değiştirmenizi sağlar. Bu ayarları temel üzerine Kod düzenleyicisinde, HTML Tasarımcısı'nın kaynak görünümü gibi diğer düzenleyiciler için de geçerlidir. Bu seçenekleri görüntülemek için seçin **seçenekleri** gelen **Araçları** menüsü. İçinde **metin düzenleyici** klasörünü genişletin **tüm diller** alt ve ardından **sekmeleri**.  
  
> [!CAUTION]
>  Bu sayfa, tüm geliştirme diller için varsayılan seçenekleri ayarlar. Bu iletişim kutusunda bir seçenek sıfırlama tüm diller sekmeler seçeneklerinde hangi seçenekler burada seçilen için sıfırlar olduğunu unutmayın. Yalnızca bir dilin metin düzenleyici seçenekleri değiştirmek için bu dil için alt klasörü genişletin ve seçeneği sayfalarını seçin.  
  
 Farklı için farklı ayarlar, belirli programlama dilleri ve ardından "Girinti ayarları birbirleriyle bireysel metin biçimleri çakışıyor için" iletisi sekmeleri seçenekler sayfaları seçilmezse, görüntülenen **Indenting**Seçenekler; ve farklı için "Birbirleriyle bireysel metin biçimleri çakışma için sekmesinde ayarları" iletisi görüntülenir **sekmesini** seçenekleri. Örneğin, bu hatırlatmayı görüntülenir **akıllı girintileme** seçeneği Visual Basic için ancak **Block girintileme** Visual C++ için seçilir.  
  
> [!NOTE]
>  Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [Visual Studio'da geliştirme ayarlarını özelleştirme](http://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
## <a name="indenting"></a>Girintileme  
 Hiçbiri  
 Bu onay kutusu seçildiğinde, yeni satırları girintili değil. Ekleme noktasını yeni bir satırın ilk sütuna yerleştirilir.  
  
 Blok  
 Bu onay kutusu seçildiğinde, yeni satırları otomatik olarak girintilenir. Ekleme noktasını önceki satırla aynı başlangıç noktasına yerleştirilir.  
  
 Akıllı  
 Seçili olduğunda, yeni satır biçimlendirme ayarları ve IntelliSense kuralları geliştirme dilini için başka bir kod her kod bağlamı uyacak şekilde yerleştirilir. Bu seçenek, tüm geliştirme diller için kullanılabilir değildir.  
  
 Örneğin, satırlar bir açılış ayracı ({}) arasında bir kapanış ayracından (}) içine otomatik olarak olabilir bir ek sekme durağı hizalanmış küme ayraçları konumundan girintili.  
  
## <a name="tabs"></a>Sekmeleri  
 Sekme boyutu  
 Ayarlar sekmesinde arasındaki boşluklar cinsinden uzaklık durdurur. Dört alan varsayılandır.  
  
 Girinti boyutu  
 Otomatik bir girinti boşluklara boyutunu ayarlar. Dört alan varsayılandır. Belirtilen boyut doldurmak için sekme karakterleri, boşluk karakteri veya her ikisi de eklenir.  
  
 Boşluklar Ekle  
 Seçildiğinde sekme karakterleri yalnızca boşluk karakterleri girinti işlemleri ekleyin. Varsa **Rintileme boyutu** ayarlanır SEKME tuşuna basın her 5, örneğin, ardından beş boşluk karakterleri eklenir veya **Girintiyi** düğmesini **biçimlendirme** araç çubuğu.  
  
 Sekmeleri tut  
 Seçili olduğunda, girinti işlemlerini mümkün olduğunca çok sekme karakterlerini ekleyin. Her sekme karakteri belirtilen boşluk sayısını doldurur **sekme boyutu**. Varsa **Rintileme boyutu** bir çift katı değil **sekme boyutu**, fark doldurmak için boşluk karakteri eklenir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Seçenekler, metin düzenleyici, tüm diller](../../ide/reference/options-text-editor-all-languages.md)   
 [Genel, Ortam, Seçenekler İletişim Kutusu](../../ide/reference/general-environment-options-dialog-box.md)
