---
title: Öğesi dizeleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Strings element (VSCT XML schema)
- VSCT XML schema elements, Strings
ms.assetid: 23a42074-a689-481d-824f-b43aa448f266
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 277cd2b8e40dfbfd1e222975f41bd4ac95c70c62
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66331721"
---
# <a name="strings-element"></a>Strings Öğesi
Strings öğesi en az bir içermesi **ButtonText** alt öğesi. Diğer tüm alt öğeler isteğe bağlıdır. Geçersiz XML karakterleri gibi '&' ve ' <' varlıklar olarak kodlanmış olmalıdır ('&amp;'ve'&lt;' vb.).

 Metin dizesindeki bir ampersan komut için klavye kısayolunu belirtir.

## <a name="syntax"></a>Sözdizimi

```
<Strings>
  <ButtonText>... </ButtonText>
  <CommandName>... </CommandName>
</Strings>
```

## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.

### <a name="attributes"></a>Öznitelikler

|Öznitelik|Açıklama|
|---------------|-----------------|
|dil|İsteğe bağlı. Dil = ".".|

### <a name="child-elements"></a>Alt Öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|ButtonText|Bu alan ve bir komut tanımı beş aşağıdaki metin alanları görüntülenen metni çeşitli menülerde belirtmenizi sağlar. Varsayılan olarak, `ButtonText` alanı denetleyicileri menü görüntülenir. `ButtonText` Alan diğer metin alanları boş ise varsayılan ayrıca olur. `ButtonText` Diğer metin alanları belirtilmiş olsa bile alan boş olamaz.|
|Tooltıptext|`ToolTipText` Alan menü öğesi için araç ipucunda görüntülenen metni belirtir.<br /><br /> Varsa `ToolTipText` alan boşsa `ButtonText` alanı kullanılır.|
|MenuText|`MenuText` Alanı ana menüsünde bir kısayol menüsü ya da bir alt araç çubuğu ise bir komut için görüntülenen metni belirtir. Varsa `MenuText` alan boşsa, tümleşik geliştirme ortamı (IDE) kullanan `ButtonText` alan. `MenuText` Alan yerelleştirme için de kullanılabilir.<br /><br /> Kısayol menüleri için `MenuText` IDE içindeki kısayol menüleri özelleştirmesini sağlar kısayol menülerini araç çubuğunda görüntülenen ad alanıdır. Bu nedenle, kısayol menüsünü ad içinde belirli bir değer; Örneğin, "Kısayol" yerine "pencere öğesi paket kısayol menüsü" kullanın.<br /><br /> Varsa `MenuText` alanı belirtilmedi, `ButtonText` alanı kullanılır.|
|commandName|`CommandName` Alan klavye kategorisinde görüntülenen metni belirtir **komutları** sekmesinde **Özelleştir** iletişim kutusu (tıklatılarak **Özelleştir**üzerinde **Araçları** menü).|
|CanonicalName|İngilizce `CanonicalName` alan girilebilir İngilizce metni komut adını belirtir **komut** pencere menü öğesi yürütülecek. IDE harf, rakam, alt çizgi veya katıştırılmış nokta olmayan tüm karakterleri kaldırır. Bu metin için birleştirilir `ButtonText` komutu tanımlamak için alan. Örneğin, **yeni proje** üzerinde **dosya** menü komutu File.NewProject haline gelir.<br /><br /> İngilizce `CanonicalName` alanı belirtilmedi, IDE kullanır `ButtonText` alan ve harf, rakam, alt çizgi ve katıştırılmış nokta dışındaki tüm şeritler. Örneğin, düğme metnini DefineCommands burada ve işareti, boşluk ve üç nokta kaldırıldığında, "& tanımla komutları..." olur.<br /><br /> Varsa `TextChanges` bayrağı belirtildi ve komut metni değiştirildiğinde, karşılık gelen komutun tarafından tanınan **komut** penceresi değiştirmez; kurallı biçimi özgün kalır `ButtonText` veya İngilizce `CanonicalName` alanları.|
|LocCanonicalName|`LocCanonicalName` Alan aynı şekilde davrandığını İngilizce'ye `CanonicalName` alan belirtilmesi yerelleştirilmiş komut metni ancak sağlar. Her iki kurallı alanlar belirtilebilir. IDE, girdiğiniz metin yalnızca ayrıştırması nedeniyle **komut** penceresi ve hem İngilizce hem de İngilizce olmayan metin komutu ile ilişkilendirilebilir aynı komutu ile ilişkilendirir.|

### <a name="parent-elements"></a>Üst Öğeler

|Öğe|Açıklama|
|-------------|-----------------|
|[Button Öğesi](../extensibility/button-element.md)|Kullanıcının etkileşime geçtiği bir öğe tanımlar.|
|[Menu Öğesi](../extensibility/menu-element.md)|Tek menü öğesini tanımlar.|
|[Combos Öğesi](../extensibility/combo-element.md)|Bir açılan kutunun içinde görünen komutlar tanımlar.|

## <a name="see-also"></a>Ayrıca Bkz.
- [Visual Studio Komut Tablosu (.Vsct) Dosyaları](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)