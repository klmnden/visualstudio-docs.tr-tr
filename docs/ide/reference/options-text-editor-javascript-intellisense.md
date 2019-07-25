---
title: Seçenekler, Metin Düzenleyici, JavaScript, IntelliSense
ms.date: 10/29/2018
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.JavaScript.Intellisense.References
- VS.ToolsOptionsPages.Text_Editor.JavaScript.Intellisense.General
- VS.ToolsOptionsPages.Text_Editor.TypeScript.IntelliSense.General
ms.assetid: b4a9816d-cf87-4dc6-a8d4-1591d6a48103
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 982c44b93ae5e3184a0c4c25e1e0a1c47f4c5e94
ms.sourcegitcommit: 85d66dc9fea3fa49018263064876b15aeb6f9584
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/24/2019
ms.locfileid: "68461735"
---
# <a name="options-text-editor-javascript-intellisense"></a>Seçenekler, Metin Düzenleyici, JavaScript, IntelliSense

JavaScript için IntelliSense davranışını etkileyen ayarları değiştirmek için **Seçenekler** Iletişim kutusunun **IntelliSense** sayfasını kullanın. **IntelliSense** sayfasına, menü çubuğunda **Araçlar** > **Seçenekler** ' i ve ardından **metin Düzenleyicisi** > **JavaScript** > IntelliSense ' i genişleterek erişebilirsiniz **.**

[!INCLUDE[note_settings_general](../../data-tools/includes/note_settings_general_md.md)]

**IntelliSense** sayfası aşağıdaki bölümleri içerir:

## <a name="statement-completion"></a>Deyim Tamamlama
 IntelliSense deyim tamamlama davranışını değiştirmek için bu seçenekleri kullanabilirsiniz.

### <a name="uielement-list"></a>UIElement Listesi
 **Yalnızca Tab veya ENTER tuşlarını kullanarak işleyin**

 Bu onay kutusunu seçtiğinizde, JavaScript kod Düzenleyicisi, yalnızca **sekmeyi** seçtikten veya anahtarı **girdikten** sonra tamamlama listesinde seçilmiş öğeler içeren deyimleri ekler. Bu onay kutusunun işaretini kaldırdığınızda nokta, virgül, iki nokta, açık parantez ve açık küme ayracı ({) gibi diğer karakterler de seçili öğelerle deyimler eklenebilir.

## <a name="references"></a>Referanslar
 Farklı JavaScript projesi türleri için kapsamda olan IntelliSense .js türlerini belirtmek için bu seçenekleri kullanabilirsiniz. IntelliSense başvuruları normalde, genel nesneler için IntelliSense desteği sağlamak amacıyla kullanılır. Bu sayfayı, çalışma zamanında yüklenmesi gereken komut dosyalarının yüklenme sırasını ayarlamak ve IntelliSense uzantı dosyalarını eklemek için de kullanabilirsiniz.

### <a name="uielement-list"></a>UIElement Listesi
 **Başvuru grupları**

 Bu seçenek başvuru grubu türünü belirtir. Üç başvuru grubu desteklenir:

 Belirli IntelliSense .js dosyalarının farklı JavaScript projeleri için kapsamda olduğunu belirtmek için önceden tanımlı başvuru gruplarını kullanabilirsiniz. Dört başvuru grubu mevcuttur:

- JavaScript kullanan uygulamalar için [!INCLUDE[win8_appname_long](../../debugger/includes/win8_appname_long_md.md)] örtük (Windows sürümü). Bu gruba eklenen dosyalar, JavaScript kullanan uygulamalar için [!INCLUDE[win8_appname_long](../../debugger/includes/win8_appname_long_md.md)] kod Düzenleyicisi 'nde açılan her. js dosyası için kapsamdadır.

- Örtük (Web); HTML5 projeleri için. Bu grupta yer alan dosyalar, bu proje türleri için Kod Düzenleyicisi'nde açılan her .js dosyası için kapsama girer.

- HTML5 Web çalışanları için adanmış çalışan başvuru grupları. Bu grupta belirtilen dosyalar, bir adanmış çalışan başvuru grubuna dair açık başvuru içeren .js dosyaları için kapsama girer.

- Genel; diğer JavaScript proje türleri için.

**Dahil edilen dosyalar**

Bu seçenek, dil hizmetinin bağlamına dosyaların yüklendiği sırayı belirtir. Sıralamayı, **Kaldır**, **Yukarı taşı**ve **aşağı taşı** düğmelerini kullanarak yapılandırabilirsiniz. IntelliSense'in düzgün çalışması için, bir diğer dosyaya bağımlı olan dosya söz konusu bu diğer dosyadan sonra yüklenmelidir.

> [!CAUTION]
> Bir nesne iki veya daha fazla örtük başvuruda koşulsuz olarak tanımlanırsa, nesneyi tanımlamak için bu listedeki son başvuru kullanılır.

**Gruba bir başvuru ekleyin**

Bu seçenek, uygun dosyaların bulunduğu yere giderek ek IntelliSense .js dosyalarını eklemek için bir yol sağlar.

**Çeşitli dosyalar projesindeki dosyalar için Uzak başvuruları (ör. http://) İndir**

Bu onay kutusu seçildiğinde ve bir proje bağlamı dışında açılmış bir JavaScript dosyanız varsa, Visual Studio IntelliSense bilgilerini sağlamak amacıyla dosyada başvurulan uzak JavaScript dosyalarını indirir. Bu seçenek işaretliyse, JavaScript dosyanıza bir başvuru olarak dahil edildiğinde dosyalar indirilir.

> [!NOTE]
> Web projeleri için, projenizde başvurulan uzak dosyalar varsayılan olarak indirilir.

## <a name="see-also"></a>Ayrıca bkz.

- [JavaScript IntelliSense](../../ide/javascript-intellisense.md)