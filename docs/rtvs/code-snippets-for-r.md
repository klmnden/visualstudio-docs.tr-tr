---
title: R için kod parçacıkları
description: Kod parçacıkları Visual Studio'da R için hızlı bir şekilde kod blokları, benzer bir kod tekrar tekrar yeniden yazmayı önlemenize yardımcı, rastgele uzunlukta eklemek için kısayollar sağlayın.
ms.date: 01/24/2018
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: jillfra
ms.workload:
- data-science
ms.openlocfilehash: 05a21da94dd643b04cea94b7840ca26d9379cb5a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62969468"
---
# <a name="code-snippets"></a>Kod parçacıkları

Visual Studio'da kod parçacıkları, hızlı bir şekilde kod blokları, benzer bir kod tekrar tekrar yeniden yazmayı önlemenize yardımcı, rastgele uzunlukta eklemek için kısayollar sağlayın. R araçları için Visual Studio (RTVS) yararlı R kod parçacıkları onlarca Visual Studio'nun koleksiyona ekleyin.

Bir kod parçacığını eklemek için kısaltılmış adını yazın (IntelliSense sağlanır) kod parçacığı, tuşuna **sekmesini** eklenecek.

Bazı basit örnekler:

- tür `=` sekmesini ardından ve RTVS genişletir kendisine `<-` atama işleci.
- tür `>` RTVS genişletir ve ardından sekme `%>%` yöneltme işleci.

Kod parçacıkları, çok daha fazlasına karakter tamamlama karakter olabilir. İçeren bir CSV dosyası okunurken bir kod parçacığı `read.csv` işlevi, örneğin, hafifletmek, parametreleri ve adları unutmayın zorunda kalmaktan:

![Animasyon read.csv çağrı eklemek için kod parçacığı kullanma](media/code-snippet-expansion.gif)

Bu durumda, siz yazarken `readc`, IntelliSense tamamlanma listesini görüntüler. Açılan menü, tamamlama seçip tuşuna basarak **sekmesini** seçer `readc`, tuşuna basarak **sekmesini** yeniden kod parçacığını genişletir. ("Kod parçacığı yazın ve SEKME tuşuna iki kez basın gibi" Bu nedenle, kod parçacığı genişletme genellikle zorlayıcı). Çoğu durumda, ilk sekme IntelliSense seçimi tamamlar ve ikinci sekme genişletme tetikler.

Kullanılabilir tüm parçacıkları görmek için **Araçları** > **kod parçacıkları Yöneticisi** iletişim kutusu (**Ctrl**+**K**,**B**) seçip **R** için **dil**. Gruplar'ı genişletin ve bir açıklama ve kısayol metnini görmek için tek tek parçacıkları seçin:

![R için kod parçacıkları iletişim kutusu](media/code-snippet-dialog.png)

Özel kod parçacıkları, yönergeleri izleyerek oluşturulacak [izlenecek yol: Kod parçacığı oluşturma](../ide/walkthrough-creating-a-code-snippet.md). Sonuç olarak, bir kod parçacığı yalnızca bir XML dosyasıdır. Örneğin, aşağıdaki kod kanal işlemi için kod parçacığı olduğunu (kısayol `>`):

```xml
<?xml version="1.0" encoding="utf-8" ?>
<CodeSnippets  xmlns="http://schemas.microsoft.com/VisualStudio/2005/CodeSnippet">
  <CodeSnippet Format="1.0.0">
    <Header>
      <Title>Dplyr pipe</Title>
      <Shortcut>&gt;</Shortcut>
      <Description>Code snippet for '%&gt;%' operator</Description>
      <Author>Microsoft Corporation</Author>
      <SnippetTypes>
        <SnippetType>Expansion</SnippetType>
       </SnippetTypes>
    </Header>
    <Snippet>
      <Code Language="R">
        <![CDATA[ %>% $end$]]>
      </Code>
    </Snippet>
  </CodeSnippet>
</CodeSnippets>
```

Tüm kod parçacıkları için XML dosyaları ile RTVS yüklenir; **konumu** alanındaki **kod parçacıkları Yöneticisi** yolunu sağlar. Github'da altında RTVS kaynak kodunda da bulabilirsiniz [src/paket/Impl/kod parçacıkları](https://github.com/Microsoft/RTVS/tree/master/src/Package/Impl/Snippets).
