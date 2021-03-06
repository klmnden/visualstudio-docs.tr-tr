---
title: Dosyalar için derleme eylemleri
ms.date: 11/19/2018
ms.technology: vs-ide-compile
ms.topic: reference
author: ghogen
ms.author: ghogen
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 35136ac0b7b0104f1812df7a9bf8ba81f6907374
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71254430"
---
# <a name="build-actions"></a>Derleme eylemleri

Visual Studio projesindeki tüm dosyaların bir yapı eylemi vardır. Yapı eylemi, proje derlendiğinde dosyaya ne olacağını denetler.

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz. [Mac için Visual Studio Içindeki derleme eylemleri](/visualstudio/mac/build-actions).

## <a name="set-a-build-action"></a>Yapı eylemi ayarla

Bir dosyaya yönelik derleme eylemini ayarlamak için, **Çözüm Gezgini** dosya ' da bir dosyayı seçip **alt**+**ENTER**' a basarak **Özellikler** penceresinde dosyanın özelliklerini açın. Ya da **Çözüm Gezgini** ' de dosyaya sağ tıklayıp **Özellikler**' i seçin. **Özellikler** penceresinde, **Gelişmiş** bölümünde, dosya için derleme eylemi ayarlamak için **Oluştur eylemi** ' nin yanındaki açılan listeyi kullanın.

![Visual Studio 'da bir dosya için derleme eylemleri](media/build-actions.png)

## <a name="build-action-values"></a>Derleme eylemi değerleri

Ve Visual Basic proje dosyaları için C# daha yaygın derleme eylemlerinden bazıları şunlardır:

|Derleme eylemi | Proje türleri | Açıklama |
|-|-|
| **AdditionalFiles** | C#, Visual Basic | Giriş olarak C# veya Visual Basic derleyicisine geçirilen kaynak olmayan bir metin dosyası. Bu derleme eylemi, genellikle kod kalitesini doğrulamak üzere bir proje tarafından başvurulan [çözümleyiciler](../code-quality/roslyn-analyzers-overview.md) için giriş sağlamak üzere kullanılır. Daha fazla bilgi için bkz. [ek dosyaları kullanma](https://github.com/dotnet/roslyn/blob/master/docs/analyzers/Using%20Additional%20Files.md).|
| **ApplicationDefinition** | WPF | Uygulamanızı tanımlayan dosya. İlk kez bir proje oluşturduğunuzda, bu *app. xaml*' dir. |
| **CodeAnalysisDictionary** | .NET | Yazım denetimi için kod analizi tarafından kullanılan özel bir sözcük sözlüğü. Bkz [. nasıl yapılır: Kod Analizi sözlüğünü özelleştirme](../code-quality/how-to-customize-the-code-analysis-dictionary.md)|
| **Se** | Kaydedilmemiş | Dosya derleyiciye kaynak dosya olarak geçirilir.|
| **İçeriği** | .NET | **İçerik** olarak işaretlenen bir dosya, çağırarak <xref:System.Windows.Application.GetContentStream%2A?displayProperty=nameWithType>akış olarak alınabilir. ASP.NET projelerinde, bu dosyalar, dağıtıldığı sırada sitenin bir parçası olarak dahil edilir.|
| **DesignData** | WPF | Kullanıcı denetimlerinin tasarım zamanında, kukla türler ve örnek verilerle görüntülenmesini sağlamak için XAML ViewModel dosyaları için kullanılır. |
| **DesignDataWithDesignTimeCreateable** | WPF | **Designdata**gibi, ancak gerçek türler.  |
| **Gömülü kaynak** | .NET | Dosya, derlemeye gömülebilen bir kaynak olarak derleyiciye geçirilir. Derlemeden dosyayı okumak <xref:System.Reflection.Assembly.GetManifestResourceStream%2A?displayProperty=fullName> için öğesini çağırabilirsiniz.|
| **EntityDeploy** | .NET | EF yapıtlarının dağıtımını belirten Entity Framework (EF). edmx dosyaları için. |
| **Fakes** | .NET | Microsoft Fakes test çerçevesi için kullanılır. Bkz. [Microsoft Fakes kullanarak test edilen kodu yalıtma](../test/isolating-code-under-test-with-microsoft-fakes.md) |
| **Yok.** | Kaydedilmemiş | Dosya, herhangi bir şekilde derleme kapsamında değildir. Bu değer, örneğin "Benioku" dosyaları gibi belge dosyaları için kullanılabilir.|
| **Sayfa** | WPF | Çalışma zamanında daha hızlı yükleme yapmak için bir XAML dosyasını bir binary. BAML dosyasına derleyin. |
| **Kaynak** | WPF | Dosyayı *. g. resources*uzantısına sahip bir derleme bildirimi kaynak dosyasına katıştırmayı belirtir. |
| **Gölgeli** | .NET | Her satırda bir tane olmak üzere oluşturulan derleme dosya adlarının listesini içeren bir. accessor dosyası için kullanılır. Listedeki her derleme için, yalnızca orijinallere benzeyen, ancak özel yöntemler `ClassName_Accessor` yerine ortak yöntemlerle ortak sınıflar oluşturun. Birim testi için kullanılır. |
| **Giriş Ekranı** | WPF | Uygulama başlatıldığında çalışma zamanında görüntülenecek bir resim dosyasını belirtir. |
| **XamlAppDef** | Windows Workflow Foundation | Derlemeyi, gömülü iş akışıyla bir derlemede iş akışı XAML dosyası oluşturmak için yönlendirir. |

> [!NOTE]
> Ek derleme eylemleri belirli proje türleri için tarafından tanımlanabilir, bu nedenle derleme eylemlerinin listesi proje türüne bağlıdır ve değerler bu listede yer alan görünebilir.

## <a name="see-also"></a>Ayrıca bkz.

- [C# derleyici seçenekleri](/dotnet/csharp/language-reference/compiler-options/listed-alphabetically)
- [Visual Basic derleyici seçenekleri](/dotnet/visual-basic/reference/command-line-compiler/compiler-options-listed-alphabetically)
- [Derleme eylemleri (Mac için Visual Studio)](/visualstudio/mac/build-actions)
