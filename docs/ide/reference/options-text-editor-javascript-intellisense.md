---
title: Seçenekler, Metin Düzenleyici, JavaScript, IntelliSense
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.JavaScript.Intellisense.References
- VS.ToolsOptionsPages.Text_Editor.JavaScript.Intellisense.General
- VS.ToolsOptionsPages.Text_Editor.TypeScript.IntelliSense.General
ms.assetid: b4a9816d-cf87-4dc6-a8d4-1591d6a48103
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 36ca451f4585e57c430456412e1811ddb56d8adf
ms.sourcegitcommit: d462dd10746624ad139f1db04edd501e7737d51e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/29/2018
ms.locfileid: "50220397"
---
# <a name="options-text-editor-javascript-intellisense"></a>Seçenekler, Metin Düzenleyici, JavaScript, IntelliSense
Kullanım **IntelliSense** sayfasının **seçenekleri** JavaScript için IntelliSense'in davranışını etkileyen ayarları değiştirmek için iletişim kutusu. Erişebildiğiniz **IntelliSense** seçerek sayfası **Araçları**, **seçenekleri** menü çubuğu ve ardından genişletme **metin düzenleyici**,  **JavaScript**, **IntelliSense.**

[!INCLUDE[note_settings_general](../../data-tools/includes/note_settings_general_md.md)]

**IntelliSense** sayfası aşağıdaki bölümleri içerir:

## <a name="validation"></a>Doğrulama
 JavaScript düzenleyicisinin belgenizdeki sözdizimini doğrulama şekline ilişkin tercihleri ayarlamak için bu seçenekleri kullanabilirsiniz.

## <a name="uielement-list"></a>UIElement Listesi
 **Zobrazovat chyby syntaxe**

 Bu onay kutusu seçili olmadığında, JavaScript kod düzenleyicisi sözdizimi hatalarını göstermez. Kendi yazmadığınız kodla çalışıyorsanız ve sözdizimi hatalarını düzeltmeyi amaçlamıyorsanız, bu özellik kullanışlıdır.

 Bu onay kutusu işaretli olduğunda tercih yapma seçeneğine sahip **hataları uyarı olarak göster** onay kutusu.

 **Hataları uyarı olarak göster**

 Bu onay kutusu seçildiğinde, JavaScript hataları uyarı olarak gösterilir (hata listesindeki hatalar olarak değil).

 **Çeşitli dosyalar projeleri içindeki dosyaların uzak kaynaklarını (örneğin http://) indir**

 Bu onay kutusu seçiliyken ve bir projenin bağlamı dışında açılmış bir JavaScript dosyanız varsa, Visual Studio IntelliSense bilgilerini sağlamak amacıyla dosyada başvurulan uzak JavaScript dosyalarını indirir. Bu seçenek işaretliyse, JavaScript dosyanıza bir başvuru olarak eklediğiniz dosyalar indirilir.

> [!NOTE]
> Web projeleri için projenizde başvurulan uzak dosyalar varsayılan olarak yüklenir.


## <a name="statement-completion"></a>Deyim Tamamlama
 IntelliSense deyim tamamlama davranışını değiştirmek için bu seçenekleri kullanabilirsiniz.

## <a name="uielement-list"></a>UIElement Listesi
 **Yalnızca sekmesini kullanın veya işleme için girin**

 Bu onay kutusu seçildiğinde, JavaScript kod düzenleyicisi deyimlere tamamlama listesinde seçilen öğeleri ancak siz Sekme veya Enter tuşuna bastıktan sonra ekler. Bu onay kutusu seçili olmadığında nokta, virgül, iki nokta üst üste, açılış parantezi ve açılış ayracı ({) da deyimlere seçili öğeleri ekleyebilir.

## <a name="references"></a>Referanslar
 Farklı JavaScript projesi türleri için kapsamda olan IntelliSense .js türlerini belirtmek için bu seçenekleri kullanabilirsiniz. IntelliSense başvuruları normalde, genel nesneler için IntelliSense desteği sağlamak amacıyla kullanılır. Bu sayfayı, çalışma zamanında yüklenmesi gereken komut dosyalarının yüklenme sırasını ayarlamak ve IntelliSense uzantı dosyalarını eklemek için de kullanabilirsiniz.

## <a name="uielement-list"></a>UIElement Listesi
 **Başvuru grupları**

 Bu seçenek başvuru grubu türünü belirtir. Üç başvuru grubu desteklenir:

 Belirli IntelliSense .js dosyalarının farklı JavaScript projeleri için kapsamda olduğunu belirtmek için önceden tanımlı başvuru gruplarını kullanabilirsiniz. Dört başvuru grubu mevcuttur:

- Örtük (Windows *sürüm*), için [!INCLUDE[win8_appname_long](../../debugger/includes/win8_appname_long_md.md)] JavaScript kullanan uygulamalar. Bu grupta yer alan dosyalar, Kod Düzenleyicisi'nde için açılan her .js dosyası için kapsama [!INCLUDE[win8_appname_long](../../debugger/includes/win8_appname_long_md.md)] JavaScript kullanan uygulamalar.

- Örtük (Web); HTML5 projeleri için. Bu grupta yer alan dosyalar, bu proje türleri için Kod Düzenleyicisi'nde açılan her .js dosyası için kapsama girer.

- Adanmış çalışan başvuru grupları; HTML5 web çalışanları. Bu grupta belirtilen dosyalar, bir adanmış çalışan başvuru grubuna dair açık başvuru içeren .js dosyaları için kapsama girer.

- Genel; diğer JavaScript proje türleri için.

**Eklenen dosyalar**

Bu seçenek, dil hizmetinin bağlamına dosyaların yüklendiği sırayı belirtir. Sırayı kullanarak yapılandırabilirsiniz **Kaldır**, **Yukarı Taşı**, ve **Aşağı Taşı** düğmeleri. IntelliSense'in düzgün çalışması için, bir diğer dosyaya bağımlı olan dosya söz konusu bu diğer dosyadan sonra yüklenmelidir.

> [!CAUTION]
> Bir nesne iki veya daha fazla örtük başvuruda koşulsuz olarak tanımlanırsa, nesneyi tanımlamak için bu listedeki son başvuru kullanılır.


**Grup bir başvuru ekleyin**

Bu seçenek, uygun dosyaların bulunduğu yere giderek ek IntelliSense .js dosyalarını eklemek için bir yol sağlar.

## <a name="see-also"></a>Ayrıca Bkz.

- [JavaScript IntelliSense](../../ide/javascript-intellisense.md)