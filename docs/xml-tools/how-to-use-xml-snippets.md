---
title: XML kod parçacıklarını kullanma
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 3a27375b-81cc-48f6-a884-e1cb8c4f78f5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d892ba202a73560568bdb6c43427a8ee0f7c1aee
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55913632"
---
# <a name="how-to-use-xml-snippets"></a>Nasıl yapılır: XML kod parçacıklarını kullanma

XML Düzenleyicisi kısayol menüsünde aşağıdaki iki komutu kullanarak XML kod parçacıklarını çağırabilirsiniz. **Parçacık Ekle** komut İmleç konumuna XML kod parçacığı ekler. **Surround With** komut XML kod parçacığı seçili metin etrafına sarmalar. Her XML kod parçacığı, kod parçacığı türleri atadığı. Kod parçacığı türleri, kod parçacığı ile kullanılabilir olup olmadığını belirlemek **parçacık Ekle** komutu **Surround With** komut veya her ikisi de.

Düzenleyici için XML kod parçacığı eklendikten sonra kod parçacığında düzenlenebilir tüm alanlar sarı renkle vurgulanır ve imleç ilk düzenlenebilir bir alanı üzerinde konumlandırıldı.

## <a name="insert-snippet"></a>Kod parçacığı Ekle

Aşağıdaki yordamlar nasıl erişileceğini açıklar **parçacık Ekle** komutu.

> [!NOTE]
> **Parçacık Ekle** komutu klavye kısayolunu kullanılabilir de (**Ctrl**+**K**, ardından **Ctrl** + **X**).

### <a name="to-insert-snippets-from-the-shortcut-menu"></a>Kısayol menüsünden kod parçacığı eklemek için

1. XML kod parçacığı eklemek istediğiniz imleci getirin.

2. Sağ tıklayıp **parçacık Ekle**.

   Kullanılabilir XML kod parçacıklarını listesi görüntülenir.

3. Fareyi kullanarak listeden veya tuşlarına basarak ve kod parçacığı adını yazarak parçacık **sekmesini** veya **Enter**.

### <a name="to-insert-snippets-using-the-intellisense-menu"></a>IntelliSense menüsünü kullanarak kod parçacığı eklemek için

1. XML kod parçacığı eklemek istediğiniz imleci getirin.

2. Gelen **Düzenle** menüsünde **IntelliSense**ve ardından **parçacık Ekle**.

   Kullanılabilir XML kod parçacıklarını listesi görüntülenir.

3. Fareyi kullanarak listeden veya tuşlarına basarak ve kod parçacığı adını yazarak parçacık **sekmesini** veya **Enter**.

### <a name="to-insert-snippets-through-the-intellisense-complete-word-list"></a>Tam sözcük IntelliSense listesinde kod parçacığı eklemek için

1. XML kod parçacığı eklemek istediğiniz imleci getirin.

2. Dosyanıza eklemek istediğiniz XML kod parçacığı yazmaya başlayın. Otomatik tamamlama açıksa, IntelliSense tam sözcük listesi görüntülenir. Görünmüyorsa, basın **Ctrl**+**alanı** etkinleştirin.

3. XML kod parçacığı tam sözcük listeden seçin.

4. Tuşuna **sekmesini**, **sekmesini** XML kod parçacığı çağırmak için.

> [!NOTE]
> XML kod parçacığı çağrılmayacağı durumlar olabilir. Örneğin, eklemeye çalışırsanız bir `xs:complexType` öğesi içinde bir `xs:element` düğüm, düzenleyici XML kod parçacığı oluşturmaz. Olduğunda bir `xs:complexType` öğesi içinde kullanılan bir `xs:element` düğüm, düzenleyici eklemek için herhangi bir veri içermez gerekli öznitelikleri veya alt öğeleri, yoktur.

### <a name="to-insert-snippets-using-the-shortcut-name"></a>Kısayol adı kullanarak kod parçacığı eklemek için

1. XML kod parçacığı eklemek istediğiniz imleci getirin.

2. Tür `<` Düzenleyicisi bölmesinde.

3. Tuşuna **Esc** tam sözcük IntelliSense listesini kapatın.

4. Kod parçacığı ve ENTER tuşuna kısayol adı **sekmesini** XML kod parçacığı çağırmak için.

## <a name="surround-with"></a>Şununla Çevrele

Aşağıdaki yordamlar nasıl erişileceğini açıklar **Surround With** komutu.

> [!NOTE]
> **Surround With** komutu klavye kısayolunu kullanılabilir de (**Ctrl**+**K**, ardından **Ctrl** + **S**).

### <a name="to-use-surround-with-from-the-context-menu"></a>Surround With bağlam menüsünden kullanmak için

1. XML Düzenleyicisi'nde kapsamak için metni seçin.

2. Sağ tıklayıp **Surround With**.

   XML kod parçacıklarını kullanılabilir çevreleyen listesi görüntülenir.

3. Fareyi kullanarak listeden veya tuşlarına basarak ve kod parçacığı adını yazarak parçacık **sekmesini** veya **Enter**.

### <a name="to-use-surround-with-from-the-intellisense-menu"></a>Surround With IntelliSense menüsünden kullanmak için

1. XML Düzenleyicisi'nde kapsamak için metni seçin.

2. Gelen **Düzenle** menüsünde **IntelliSense**ve ardından **Surround With**.

   XML kod parçacıklarını kullanılabilir çevreleyen listesi görüntülenir.

3. Fareyi kullanarak listeden veya tuşlarına basarak ve kod parçacığı adını yazarak parçacık **sekmesini** veya **Enter**.

## <a name="use-xml-snippets"></a>XML kod parçacıklarını kullanma

XML kod parçacığı seçtikten sonra metin kod parçacığının İmleç konumuna otomatik olarak eklenir. Kod parçacığı düzenlenebilir tüm alanlarda vurgulanır ve ilk düzenlenebilir bir alanı otomatik olarak seçilir. Şu anda seçili alanı Kutulu olmasıdır.

Bir alan seçildiğinde, alan için yeni bir değer yazabilirsiniz. Tuşuna basarak **sekmesini** parçacığının düzenlenebilir alanları arasında geçiş yapar; tuşlarına basarak **Shift**+**sekmesini** aracılığıyla ters sırada geçiş yapar. Bir alana tıklayarak alana imleci koyar ve seçen bir alana çift tıklayın. Bir alan vurgulandığında, alanın açıklaması sunan bir araç ipucu görüntülenebilir.

Yalnızca ilk örneği, belirli bir alanın düzenlenebilir. Bu alan de vurgulandığında, bu alana diğer örneklerini özetlenmiştir. Düzenlenebilir bir alanın değerini değiştirdiğinizde, bu alan kod parçacığında kullanılan her yerde değiştirilir.

Tuşuna basarak **Enter** veya **Esc** alan düzenleme iptal eder ve düzenleyici normal olarak döndürür.

Düzenlenebilir bir kod parçacığı alanlar için varsayılan renkleri değiştirerek değiştirilebilir **kod parçacığı alanı** ayarı **yazı tipleri ve renkler** bölmesinde **seçenekleri** iletişim kutusu. Daha fazla bilgi için [nasıl yapılır: Yazı tipleri ve renkler düzenleyicisinde değişiklik](../ide/reference/how-to-change-fonts-and-colors-in-the-editor.md).

## <a name="see-also"></a>Ayrıca bkz.

- [XML kod parçacıkları](../xml-tools/xml-snippets.md)
- [Nasıl yapılır: XML şemasından XML kod parçacığı oluşturma](../xml-tools/how-to-generate-an-xml-snippet-from-an-xml-schema.md)
- [Nasıl yapılır: XML kod parçacıkları oluşturma](../xml-tools/how-to-create-xml-snippets.md)