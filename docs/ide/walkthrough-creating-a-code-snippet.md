---
title: 'İzlenecek yol: Kod parçacığı oluşturma'
ms.date: 06/10/2019
ms.topic: conceptual
helpviewer_keywords:
- code snippets, creating
- code snippets, shortcut
- code snippets, template
- code snippets, replacements
- code snippets, references
- code snippets, imports
ms.assetid: 0dcaae11-39cf-4463-9c90-2494321251c2
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- VB
ms.workload:
- multiple
ms.openlocfilehash: 6f58581a601da59e7ff66a3bae5ddcb7432bf8e3
ms.sourcegitcommit: cc5fd59e5dc99181601b7db8b28d7f8a83a36bab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2019
ms.locfileid: "66836095"
---
# <a name="walkthrough-create-a-code-snippet"></a>İzlenecek yol: Kod parçacığı oluşturma

Yalnızca birkaç adımda bir kod parçacığı oluşturabilirsiniz. Tek yapmak için ihtiyacınız olan bir XML dosyası oluşturun, uygun öğeleri doldurmak ve kodunuzu ekleyin. İsteğe bağlı olarak değiştirme parametreleri kullanın ve proje başvuruları da yapabilirsiniz. Kod parçacığını kullanarak Visual Studio yüklemenizin içeri **alma** düğmesine **kod parçacıkları Yöneticisi** (**Araçları** > **kod Kod parçacıkları Yöneticisi'ni**).

## <a name="snippet-template"></a>Parçacık şablonu

Aşağıdaki XML Temel parçacık şablonu verilmiştir:

```xml
<?xml version="1.0" encoding="utf-8"?>
<CodeSnippets xmlns="http://schemas.microsoft.com/VisualStudio/2005/CodeSnippet">
    <CodeSnippet Format="1.0.0">
        <Header>
            <Title></Title>
        </Header>
        <Snippet>
            <Code Language="">
                <![CDATA[]]>
            </Code>
        </Snippet>
    </CodeSnippet>
</CodeSnippets>
```

## <a name="create-a-code-snippet"></a>Kod parçacığı oluşturma

1. Visual Studio'da yeni bir XML dosyası oluşturun ve yukarıda gösterilen şablonu ekleyin.

2. Kod parçacığında başlığını doldurun **başlık** öğesi. Başlık kullanın **kare kökünü**.

3. Kod parçacığında dilini doldurun **dil** özniteliği **kod** öğesi. İçin C#, kullanın **CSharp**ve Visual Basic için **VB**.

   > [!TIP]
   > Tüm kullanılabilir dil değerleri görmek için Gözat [kod öğe öznitelikleri bölümünü](code-snippets-schema-reference.md#attributes) üzerinde [kod parçacıkları şema başvurusu](code-snippets-schema-reference.md) sayfası.

4. Kod parçacığı Ekle **CDATA** bölümünü **kod** öğesi.

   C# için:

   ```xml
   <Code Language="CSharp">
       <![CDATA[double root = Math.Sqrt(16);]]>
   </Code>
   ```

   Veya Visual Basic için:

   ```xml
   <Code Language="VB">
       <![CDATA[Dim root = Math.Sqrt(16)]]>
   </Code>
   ```

5. Kod parçacığını olarak kaydedin *SquareRoot.snippet* (herhangi bir yere kaydetmeden).

## <a name="import-a-code-snippet"></a>Kod parçacığını İçeri Aktar

1. Visual Studio yüklemenizin bir kod parçacığını kullanarak aktarabilirsiniz **kod parçacıkları Yöneticisi**. Seçerek açın **Araçları** > **kod parçacıkları Yöneticisi**.

2. Tıklayın **alma** düğmesi.

3. Önceki yordamda kod parçacığını kaydedildiği konuma seçin ve tıklayın Git **açık**.

4. **Kod parçacığını içe aktar** iletişim kutusunu açar, sağ bölmedeki seçeneklerden parçacığın nereye isteyen. Seçeneklerden biri olmalıdır **kod Parçacıklarım**. Seçin ve **son**, ardından **Tamam**.

5. Kod parçacığı, kodun dile bağlı olarak aşağıdaki konumlardan birine kopyalanır:

   ::: moniker range="vs-2017"

   *%USERPROFILE%\Documents\Visual Studio 2017\Code Snippets\Visual C#\My Code Snippets*
    *%USERPROFILE%\Documents\Visual Studio 2017\Code Snippets\Visual Basic\My Code Snippets*

   ::: moniker-end

   ::: moniker range=">=vs-2019"

   *%USERPROFILE%\Documents\Visual Studio 2019\Code Snippets\Visual C#\My Code Snippets*
    *%USERPROFILE%\Documents\Visual Studio 2019\Code Snippets\Visual Basic\My Code Snippets*

   ::: moniker-end

6. Açarak parçacığınızı test bir C# veya Visual Basic projesi. Düzenleyicide açık bir kod dosyası ile seçin **parçacıkları** > **parçacık Ekle** sağ tıklama menüsünden **kod Parçacıklarım**. Adlı bir parçacık görmelisiniz **kare kökünü**. Çift tıklatın.

   Kod parçacığı, kod dosyasına eklenir.

## <a name="description-and-shortcut-fields"></a>Açıklama ve kısayol alanları

::: moniker range="vs-2017"

1. Açıklama alanları, kod parçacıkları Yöneticisi'nde görüntülendiğinde, kod parçacığı hakkında daha fazla bilgi verin. Kısayol, kod parçacığını eklemek için kullanıcıların yazabileceği bir etikettir. Dosyasını açarak eklediğiniz parçacığı düzenleyin *%USERPROFILE%\Documents\Visual Studio 2017\Code parçacıkları\\[Visual C# veya Visual Basic] \My Code Snippet\SquareRoot.snippet*.

::: moniker-end

::: moniker range=">=vs-2019"

1. Açıklama alanları, kod parçacıkları Yöneticisi'nde görüntülendiğinde, kod parçacığı hakkında daha fazla bilgi verin. Kısayol, kod parçacığını eklemek için kullanıcıların yazabileceği bir etikettir. Dosyasını açarak eklediğiniz parçacığı düzenleyin *%USERPROFILE%\Documents\Visual Studio 2019\Code parçacıkları\\[Visual C# veya Visual Basic] \My Code Snippet\SquareRoot.snippet*.

::: moniker-end

   > [!TIP]
   > Visual Studio yerleştirdiğiniz yere dizininde dosyasını düzenlediğinizden bu yana, Visual Studio için yeniden gerekmez.

2. Ekleme **Yazar** ve **açıklama** öğelerine **üstbilgi** öğesi ve bunları doldurun.

3. **Üstbilgi** öğesi şunun gibi görünmelidir:

   ```xml
   <Header>
       <Title>Square Root</Title>
       <Author>Myself</Author>
       <Description>Calculates the square root of 16.</Description>
   </Header>
   ```

4. Açık **kod parçacıkları Yöneticisi** ve kod parçacığınızı seçin. Sağ bölmede, dikkat **açıklama** ve **Yazar** alanlarını artık doldurulmuş.

   ![Kod parçacığı açıklama kod parçacığı Yöneticisi'nde](media/code-snippet-description-author.png)

5. Bir kısayol eklemek için Ekle bir **kısayol** öğesiyle **üstbilgi** öğesi:

   ```xml
   <Header>
      <Title>Square Root</Title>
      <Author>Myself</Author>
      <Description>Calculates the square root of 16.</Description>
      <Shortcut>sqrt</Shortcut>
    </Header>
   ```

6. Kod parçacığı dosyasını yeniden kaydedin.

7. Bir kısayolu sınamak için daha önce kullandığınız projesini açtığınızda,, yazın **sqrt** Düzenleyicisi ve tuşuna **sekmesini** (Visual Basic için bir kez için iki kez C#).

   Kod parçacığı eklenir.

## <a name="replacement-parameters"></a>Değiştirme parametreleri

Parçaları bir kod parçacığı, kullanıcı tarafından değiştirilmesini isteyebilirsiniz. Örneğin, kullanıcının kendi geçerli proje içinde bir değişken adı yerine isteyebilirsiniz. İki tür değişiklik sağlayabilirsiniz: sabit değerler ve nesneler. Kullanım [Literal öğesi](code-snippets-schema-reference.md#literal-element) tamamen kod parçacığı ancak büyük olasılıkla içinde yer alan kod parçasını (örneğin, dize veya sayısal bir değer) koda eklendikten sonra özelleştirilmesi yerine tanımlamak için. Kullanım [nesne öğesi](code-snippets-schema-reference.md#object-element) kod parçacığının gerek duyduğu, ancak büyük olasılıkla kod parçacığının kendisi dışında (örneğin, bir nesne örneği veya bir denetim) tanımlanacak bir öğeyi tanımlamak için.

1. Kullanıcının kaç kare kökünü hesaplamak için kolayca etkinleştirmek için istemcilerdeki **kod parçacığı** öğesinin *SquareRoot.snippet* aşağıdaki gibi:

   ```xml
   <Snippet>
     <Code Language="CSharp">
       <![CDATA[double root = Math.Sqrt($Number$);]]>
     </Code>
     <Declarations>
       <Literal>
         <ID>Number</ID>
         <ToolTip>Choose the number you want the square root of.</ToolTip>
         <Default>16</Default>
       </Literal>
     </Declarations>
   </Snippet>
   ```

   Değişmez değer değişikliği bir kimlik verilir dikkat edin (`Number`). Kimliği gelen içinde kod parçacığı ile çevreleyen tarafından başvuruda bulunulan `$` karakter:

   ```xml
   <![CDATA[double root = Math.Sqrt($Number$);]]>
   ```

2. Kod parçacığı dosyasını kaydedin.

3. Bir projeyi açmak ve kod parçacığını ekleyin.

   Kod parçacığı eklendikten ve düzenlenebilir değişmez değerin yerini vurgulanır. Araç İpucu değeri görmek için değiştirme parametresi üzerine gelin.

   ![Kod parçacığı değiştirme parametresi Visual Studio araç ipucunda](media/snippet-replacement-parameter-tooltip.png)

   > [!TIP]
   > Bir kod parçacığında replacable birden fazla parametre varsa, basabilirsiniz **sekmesini** birinden diğerine değerlerini değiştirmek için gidin.

## <a name="import-a-namespace"></a>Bir ad alanı alma

Kod parçacığı eklemek için kullanabileceğiniz bir `using` yönergesi (C#) veya `Imports` ekleyerek deyimi (Visual Basic) [Imports öğesi](code-snippets-schema-reference.md#imports-element). .NET Framework projeleri için de bir projeye başvuru kullanarak ekleyebileceğiniz [References öğesi](code-snippets-schema-reference.md#references-element).

Aşağıdaki XML yöntemini kullanan bir kod parçacığı gösterir `File.Exists` System.IO ad alanında ve bu nedenle, tanımlar **içeri aktarmalar** System.IO ad alanı içeri aktarmak için öğesi.

```xml
<?xml version="1.0" encoding="utf-8"?>
<CodeSnippets xmlns="http://schemas.microsoft.com/VisualStudio/2005/CodeSnippet">
  <CodeSnippet Format="1.0.0">
    <Header>
      <Title>File Exists</Title>
      <Shortcut>exists</Shortcut>
    </Header>
    <Snippet>
      <Code Language="CSharp">
        <![CDATA[var exists = File.Exists("C:\\Temp\\Notes.txt");]]>
      </Code>
      <Imports>
        <Import>
          <Namespace>System.IO</Namespace>
        </Import>
      </Imports>
    </Snippet>
  </CodeSnippet>
</CodeSnippets>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Kod parçacıkları şema başvurusu](../ide/code-snippets-schema-reference.md)