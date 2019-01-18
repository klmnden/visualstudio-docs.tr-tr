---
title: XML belgeleri yorumları Ekle
ms.date: 01/26/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 5b10a0bae3a9e3b0ce5f9135669cb788f0ddce9d
ms.sourcegitcommit: 8c4267540c0ac39664f6902c423516f408f3cbd4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/17/2019
ms.locfileid: "54380382"
---
# <a name="how-to-insert-xml-comments-for-documentation-generation"></a>Nasıl yapılır: Belgeleri oluşturmak için XML açıklamalarını ekleme

Visual Studio size yardımcı olabilir belge sınıfları ve yöntemleri gibi kod öğeleri otomatik olarak standart XML belge açıklaması yapısını oluşturarak. Derleme zamanında içeren belge yorumlarını bir XML dosyası oluşturabilirsiniz.

> [!TIP]
> Oluşturulan XML dosyasının konumunu ve adını yapılandırma hakkında daha fazla bilgi için bkz: [XML açıklamalarıyla kodunuzu belgeleme (C# Kılavuzu)](/dotnet/csharp/codedoc).

Visual Studio ve diğer Ide'leri IntelliSense türler ve üyeler hakkında hızlı bilgi göstermek için kullanabilirsiniz, böylece derleyici tarafından oluşturulan XML dosyasının yanı sıra .NET bütünleştirilmiş kodunuzda dağıtılabilir. Ayrıca, XML dosyasını gibi araçlarla çalıştırılabilir [DocFX](https://dotnet.github.io/docfx/) ve [Sandcastle](https://www.microsoft.com/download/details.aspx?id=10526) API Başvurusu Web siteleri oluşturmak için.

> [!NOTE]
> **Açıklama Ekle** XML belgeleri yorumları otomatik olarak ekleyen komutu kullanılabilir [ C# ](/dotnet/csharp/programming-guide/xmldoc/xml-documentation-comments) ve [Visual Basic](/dotnet/visual-basic/programming-guide/program-structure/how-to-create-xml-documentation). Ancak, el ile ekleyebilirsiniz [c++ XML belgeleri yorumları](/cpp/ide/xml-documentation-visual-cpp) dosyaları ve yine de derleme zamanında XML belge dosyalarını oluştur.

## <a name="to-insert-xml-comments-for-a-code-element"></a>Bir kod öğesi için XML açıklamaları eklemek için

1. Belge, örneğin, bir yöntem için istediğiniz öğeyi yukarıda metin imleci yerleştirin.

1. Aşağıdakilerden birini yapın:

   - Tür `///` içinde C#, veya `'''` Visual Basic'te

   - Gelen **Düzenle** menüsünde seçin **IntelliSense** > **Açıklama Ekle**

   - Seçin sağ tıklayın veya bağlam menüsünden veya yalnızca kod öğesi sonraki sürümlere **kod parçacığı** > **Açıklama Ekle**

   XML şablonu kod öğesi hemen oluşturulmaz. Örneğin, bir yöntem Yorum olduğunda ürettiği **\<Özet\>** öğesi, bir **\<param\>** her parametre ve bir öğesi**\<döndürür\>** dönüş değeri belge öğesi.

   ![XML açıklama şablonu-C#](media/doc-preview-cs.png)

   ![XML açıklama şablonu - Visual Basic](media/doc-preview-vb.png)

1. Her bir XML öğesinin kod öğesi tam olarak belge açıklamalarını girin.

   ![Tamamlanan açıklaması](media/doc-result-cs.png)

> [!NOTE]
> Var olan bir [seçeneği](../../ide/reference/options-text-editor-csharp-advanced.md) yazdıktan sonra geçiş XML belge açıklamaları için `///` içinde C# veya `'''` Visual Basic. Menü çubuğundan seçin **Araçları** > **seçenekleri** açmak için **seçenekleri** iletişim kutusu. Ardından, gidin **metin düzenleyici**  >  **C#** veya **temel** > **Gelişmiş**. İçinde **Düzenleyici Yardımı** bölümünde, Aranan **XML belge açıklamaları oluştur** seçeneği.

## <a name="see-also"></a>Ayrıca bkz.

- [XML belgeleri yorumları (C# Programlama Kılavuzu)](/dotnet/csharp/programming-guide/xmldoc/xml-documentation-comments)
- [XML açıklamalarıyla kodunuzu belgeleme (C# Kılavuzu)](/dotnet/csharp/codedoc)
- [Nasıl yapılır: XML belgeleri (Visual Basic) oluşturma](/dotnet/visual-basic/programming-guide/program-structure/how-to-create-xml-documentation)
- [C++ açıklamaları](/cpp/cpp/comments-cpp)
- [XML belgeleri (C++)](/cpp/ide/xml-documentation-visual-cpp)
- [Kod oluşturma](../code-generation-in-visual-studio.md)