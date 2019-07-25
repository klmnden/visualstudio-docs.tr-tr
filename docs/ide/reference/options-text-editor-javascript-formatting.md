---
title: Seçenekler, Metin Düzenleyici, JavaScript, Biçimlendirme
ms.date: 10/29/2018
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.JavaScript.Formatting.Spacing
- VS.ToolsOptionsPages.Text_Editor.JavaScript.Formatting.General
- VS.ToolsOptionsPages.Text_Editor.JavaScript.Formatting.New_Lines
- VS.ToolsOptionsPages.Text_Editor.TypeScript.Formatting.Spacing
- VS.ToolsOptionsPages.Text_Editor.TypeScript.Formatting.General
- VS.ToolsOptionsPages.Text_Editor.TypeScript.Formatting.New_Lines
ms.assetid: 28a0aef1-9353-4d94-95a5-54b42e15c0dc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b23067475c8c5ff4d858ade8443946f7d9c73afc
ms.sourcegitcommit: 85d66dc9fea3fa49018263064876b15aeb6f9584
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/24/2019
ms.locfileid: "68461344"
---
# <a name="options-text-editor-javascript-formatting"></a>Seçenekler, Metin Düzenleyici, JavaScript, Biçimlendirme
Kod düzenleyicisinde biçimlendirme kodu seçeneklerini ayarlamak için **Seçenekler** Iletişim kutusunun **biçimlendirme** sayfasını kullanın. Bu sayfaya erişmek için, menü çubuğunda **Araçlar**, **Seçenekler**' i seçin ve ardından **metin Düzenleyicisi**, **JavaScript**ve **biçimlendirme**' yi genişletin.

[!INCLUDE[note_settings_general](../../data-tools/includes/note_settings_general_md.md)]

## <a name="automatic-formatting"></a>Otomatik Biçimlendirme
 Bu seçenekler, **kaynak** görünümünde biçimlendirmenin ne zaman gerçekleşeceğini belirlenir.

### <a name="uielement-list"></a>UIElement Listesi

|Seçenek|Açıklama|
|------------|-----------------|
|**Girerken Biçimlendirme tamamlandı satırı**|Bu seçenek belirlendiğinde, Enter tuşunu seçtiğinizde, kod Düzenleyicisi otomatik olarak çizgiyi biçimlendirir.|
|**; Üzerinde biçimlendirme tamamlandı ekstresi**|Bu seçenek belirlendiğinde, noktalı virgül anahtarını seçtiğinizde, kod Düzenleyicisi otomatik olarak çizgiyi biçimlendirir.|
|**{} Üzerinde açılan blok Biçimlendir**|Bu seçenek belirlendiğinde, açılan küme ayracı anahtarını seçtiğinizde, kod Düzenleyicisi otomatik olarak çizgiyi biçimlendirir.|
|**} Üzerinde biçimlendirme tamamlandı bloğu**|Bu seçenek belirlendiğinde, kapanış küme ayracı tuşunu seçtiğinizde, kod Düzenleyicisi otomatik olarak çizgiyi biçimlendirir.|
|**Yapıştırırken Biçimlendir**|Bu seçenek belirlendiğinde kod Düzenleyicisi, düzenleyiciye yapıştırdığınızda kodu yeniden biçimlendirir. Düzenleyici, geçerli olarak tanımlanmış biçimlendirme kurallarını kullanır. Bu seçenek seçilmezse, düzenleyici yapıştırılan kodun özgün biçimlendirmesini kullanır.|

## <a name="new-lines"></a>Yeni satırlar
 Bu seçenekler, kod düzenleyicisinin yeni bir satırdaki işlevler ve denetim blokları için açık bir küme ayracı yerleştirip yerleştirmediğini belirtir.

### <a name="uielement-list"></a>UIElement Listesi

|Seçenek|Açıklama|
|------------|-----------------|
|**İşlevler için yeni satıra açık küme ayracı yerleştir**|Bu seçenek belirlendiğinde, kod Düzenleyicisi bir işlevle ilişkili açık küme ayracını yeni bir satıra taşıdır.|
|**Denetim blokları için yeni satıra açık küme ayracı yerleştir**|Bu seçenek belirlendiğinde, kod Düzenleyicisi bir denetim bloğu (örneğin, `if` ve `while` denetim blokları) ile ilişkili açık küme ayracını yeni bir satıra taşıdır.|

## <a name="spacing"></a>Aralığı
 Bu seçenekler, **kaynak** görünümünde boşlukların nasıl ekleneceğini tespit ediyor.

### <a name="uielement-list"></a>UIElement Listesi

|Seçenek|Açıklama|
|------------|-----------------|
|**Virgül sınırlayıcısından sonra boşluk Ekle**|Bu seçenek belirlendiğinde, kod Düzenleyicisi virgül sınırlayıcıdan sonra bir boşluk ekler.|
|**' For ' deyimlerinde noktalı virgülden sonra boşluk Ekle**|Bu seçenek belirlendiğinde, kod Düzenleyicisi `for` döngünün ilk satırına her noktalı virgülden sonra bir boşluk ekler.|
|**İkili işleçlerden önce ve sonra boşluk Ekle**|Bu seçenek belirlendiğinde, kod Düzenleyicisi ikili işleçlerden önce ve sonra bir boşluk ekler (örneğin, +,-, & &, &#124; &#124;).|
|**Denetim akışı deyimlerinde anahtar sözcüklerden sonra boşluk Ekle**|Bu seçenek belirlendiğinde, kod Düzenleyicisi denetim akış deyimlerindeki JavaScript anahtar sözcükleriyle sonra bir boşluk ekler.|
|**Anonim işlevler için Function anahtar sözcüğünden sonra boşluk Ekle**|Bu seçenek belirlendiğinde, kod Düzenleyicisi anonim işlevler için `function` anahtar sözcükten sonra bir boşluk ekler.|
|**Boş olmayan parantezleri kapatmadan önce ve açtıktan sonra boşluk Ekle**|Bu seçenek belirlendiğinde, kod Düzenleyicisi, parantez içinde boş olmayan karakterler varsa, açma parantezinden sonra ve kapatma parantezinden önce bir boşluk ekler.|

## <a name="see-also"></a>Ayrıca Bkz.

- [Genel, Ortam, Seçenekler İletişim Kutusu](../../ide/reference/general-environment-options-dialog-box.md)