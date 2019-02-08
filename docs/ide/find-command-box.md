---
title: Bul-komut kutusu
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.findcommandbox
helpviewer_keywords:
- Find/Command box
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 221c5fbbd3f0f82ac97d0c2a0fcc82657e0296c4
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55906689"
---
# <a name="findcommand-box"></a>Bul/Komut kutusu

Arama metni ve Visual Studio komutları çalıştırmak **Bul/komut** kutusu. **Bul/komut** kutusu araç çubuğu denetimi olarak hala kullanılabilir, ancak artık varsayılan olarak görünür. Görüntüleyebileceğiniz **Bul/komut** kutusunu **Düğme Ekle veya Kaldır** üzerinde **standart** araç çubuğu ve ardından **Bul**.

Çalıştırılacak bir [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] komutu, bir büyük yazdığınızdan değerinden (**>**) oturum.

**Bul/komut** kutusuna girilen son 20 öğe korur ve bunları bir aşağı açılan listede görüntüler. Listede seçerek gidebilirsiniz **ok tuşlarını**.

![Bulma&#47;komut kutusu](../ide/media/findcommandbox.png)

## <a name="searching-for-text"></a>Metin arama

Varsayılan olarak metin belirttiğinizde **Bul/komut** kutusuna ve ardından **Enter** anahtar, Visual Studio içinde belirtilenseçeneklerikullanarakgeçerlibelgeveyaaraçpenceresininarar**Dosyalarda Bul** iletişim kutusu. Daha fazla bilgi için [bulma ve değiştirme metni](../ide/finding-and-replacing-text.md).

## <a name="entering-commands"></a>Komutlar girme

Kullanılacak **Bul/komut** tek bir sorun için onay kutusunu [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] komutunu ya da diğer ad komutu büyük bir metin arama yerine yazdığınızdan değerinden (**>**) simgesi. Örneğin:

```
>File.NewFile c:\temp\MyFile /t:"General\Text File"
```

Alternatif olarak, ayrıca kullanabileceğiniz **komut** girin ve tek veya birden çok komut yürütme penceresi. Bazı komutlar veya diğer adlar girilen ve kendileri tarafından yürütülen; diğerleri kendi sözdizimi değişkenlerinde gerek duyarlar. Bağımsız değişkenlere sahip komutları listesi için bkz. [Visual Studio komutları](../ide/reference/visual-studio-commands.md).

## <a name="escape-characters"></a>Kaçış karakterleri

Şapka işareti (**^**) bir komut karakter anlamına karakter hemen sonrasında yerine birebir yorumlandığı bir denetim karakteri olarak yorumlanır. Bu düz tırnak işaretleri eklemek için kullanılabilir (**"**), boşluk, önde gelen eğik çizgiler, düzeltme işaretleri veya herhangi başka bir sabit karakterin bir parametre veya anahtar değeri, anahtar adları dışında. Örneğin:

```
>Edit.Find ^^t /regex
```

İç veya dış tırnak işaretleri olup olmadığını şapka işareti aynı şekilde çalışır. Şapka işareti satırdaki son karakterse, yoksayılır.

## <a name="see-also"></a>Ayrıca bkz.

- [Komut penceresi](../ide/reference/command-window.md)
- [Metin bulma ve değiştirme](../ide/finding-and-replacing-text.md)