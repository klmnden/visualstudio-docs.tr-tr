---
title: Kod parçacıkları
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.ExpansionManagerImport
- vs.codesnippetmanager
helpviewer_keywords:
- surround with
- code snippets
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
- CPP
ms.workload:
- multiple
ms.openlocfilehash: 89de993337ecd214c7771faf17b24f90fa5e0110
ms.sourcegitcommit: 0f44ec8ba0263056ad04d2d0dc904ad4206ce8fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2019
ms.locfileid: "70766251"
---
# <a name="code-snippets"></a>Kod parçacıkları

Kod parçacıkları, sağ tıklama menüsü (bağlam menüsü) komutu veya kısayol tuşlarının birleşimini kullanarak bir kod dosyasına eklenebilen yeniden kullanılabilir kod bloklarında yer alabilir. Genellikle, `try-finally` veya `if-else` blokları gibi yaygın olarak kullanılan kod blokları içerirler, ancak tüm sınıfları veya yöntemleri eklemek için kullanılabilirler.

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz. [kod parçacıkları (Mac için Visual Studio)](/visualstudio/mac/snippets).

Kod parçacıkları,, Visual Basic, XML ve T-SQL dahil C#olmak C++üzere çok sayıda dilde kullanılabilir ve birkaç kez ad verebilir. Bir dile ait kullanılabilir tüm yüklü parçacıkları görüntülemek için, **Araçlar** menüsünden **kod parçacıkları Yöneticisi 'ni** açın (veya **CTRL**+**K**, **CTRL**+**B**tuşlarına basın) ve şu dil arasından En üstteki açılan menü.

![Kod parçacıkları Yöneticisi iletişim kutusu](media/code-snippets-manager.png)

Kod parçacıklarına aşağıdaki genel yollarla erişilebilir:

- Menü çubuğunda, > **IntelliSense** > Düzenle**kod parçacığı Ekle** ' yi seçin.

- Kod düzenleyicisindeki sağ tıklama veya bağlam menüsünde kod **parçacığı** > **ekleme kod parçacığı** ' ni seçin.

- Klavyeden **CTRL**+**K**,**CTRL**+**X** tuşlarına basın

## <a name="expansion-snippets-and-surround-with-snippets"></a>Genişleme parçacıkları ve surround-kod parçacıkları

Visual Studio 'da, belirtilen bir ekleme noktasına eklenen ve bir kod parçacığı kısayolunun yanı sıra (yalnızca ve yalnızca) kod parçacığı kısayolunu ve birlikte çevrelemeyi (C# yalnızca ve C++ yalnızca) içerebilen bir kod parçacığı olan iki tür kod parçacığı vardır.

Genişletme kod parçacığına bir örnek: C# tryf kısayolunun bir try-finally bloğu eklemek için kullanılır:

```csharp
try
{

}
finally
{

}
```

Kod penceresinin sağ tıklama menüsünde (bağlam menüsü) kod **parçacığı Ekle** ' `tryf` **C#** ye tıklayıp, ardından yazarak ve ardından ENTER tuşuna basarak bu kod parçacığını ekleyebilirsiniz. İsterseniz Tab tuşuna iki kez `tryf` yazabilir ve basabilirsiniz.

C++ ,`if` Bir ekleme kod parçacığı ya da bir surround, kod parçacığı olarak birlikte kullanılabilir. Bir kod `return FALSE;`satırı seçer (örneğin) ve ardından **birlikte** > Çevrele seçeneğini belirlerseniz, kod parçacığı satır etrafında genişletilir:

```cpp
if (true)
{
    return FALSE;
}
```

## <a name="snippet-replacement-parameters"></a>Kod parçacığı değiştirme parametreleri

Kod parçacıkları, yazmakta olduğunuz kesin kodu sığdırmak için değiştirmeniz gereken yer tutucuları olan değiştirme parametrelerini içerebilir. Önceki örnekte `true` , uygun koşulla değiştireceğiniz bir değiştirme parametresidir. Yaptığınız değişiklik, kod parçacığında aynı değiştirme parametresinin her örneği için yinelenir.

Örneğin, Visual Basic bir özelliği ekleyen bir kod parçacığı vardır. Kod parçacığını eklemek için, bir Visual Basic kod dosyasındaki sağ tıklama veya bağlam menüsünden **kod parçacığı** > **Ekle kod parçacığını** seçin. Ardından, **kod desenleri** > **özelliklerini, yordamları, olayları** > **bir özelliği tanımlar**.

![Özellik tanımlamak için kod parçacığı menüsü](media/code-snippets-vb-property.png)

Aşağıdaki kod eklenir:

```vb
Private newPropertyValue As String
Public Property NewProperty() As String
    Get
        Return newPropertyValue
    End Get
    Set(ByVal value As String)
        newPropertyValue = value
    End Set
End Property
```

' A geçiş `newPropertyValue` yaparsanız,herörneğideğiştirilir.`newPropertyValue` `m_property` Özelliğini özellik bildiriminde `String` olarak `Int` değiştirirseniz, set yöntemindeki değer de olarak `Int`değiştirilir.

## <a name="see-also"></a>Ayrıca bkz.

- [İzlenecek yol: Kod parçacığı oluşturma](../ide/walkthrough-creating-a-code-snippet.md)
- [Nasıl yapılır: Kod parçacıklarını dağıtma](../ide/how-to-distribute-code-snippets.md)
- [Kod parçacıkları kullanmak için en iyi uygulamalar](../ide/best-practices-for-using-code-snippets.md)
- [Sorun giderme parçacıkları](../ide/troubleshooting-snippets.md)
- [C#kod parçacıkları](../ide/visual-csharp-code-snippets.md)
- [Görsel C++ kod parçacıkları](../ide/visual-cpp-code-snippets.md)
- [Kod parçacıkları şema başvurusu](../ide/code-snippets-schema-reference.md)
- [Kod parçacıkları (Mac için Visual Studio)](/visualstudio/mac/snippets)
