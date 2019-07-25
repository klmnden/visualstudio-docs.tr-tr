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
ms.openlocfilehash: 061a3cce8d1d29b57c02de4506a809994bf12910
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68416504"
---
# <a name="build-actions"></a>Derleme eylemleri

Visual Studio projesindeki tüm dosyaların bir yapı eylemi vardır. Yapı eylemi, proje derlendiğinde dosyaya ne olacağını denetler.

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz. [Mac için Visual Studio Içindeki derleme eylemleri](/visualstudio/mac/build-actions).

## <a name="set-a-build-action"></a>Yapı eylemi ayarla

Bir dosyaya yönelik derleme eylemini ayarlamak için, **Çözüm Gezgini** dosya ' da bir dosyayı seçip **alt**+**ENTER**' a basarak **Özellikler** penceresinde dosyanın özelliklerini açın. Ya da **Çözüm Gezgini** ' de dosyaya sağ tıklayıp **Özellikler**' i seçin. **Özellikler** penceresinde, **Gelişmiş** bölümünde, dosya için derleme eylemi ayarlamak için **Oluştur eylemi** ' nin yanındaki açılan listeyi kullanın.

![Visual Studio 'da bir dosya için derleme eylemleri](media/build-actions.png)

## <a name="build-action-values"></a>Derleme eylemi değerleri

Ve Visual Basic proje dosyaları için C# bazı derleme eylemleri şunlardır:

* **Hiçbiri** -dosya, herhangi bir şekilde derleme kapsamında değildir. Bu değer, örneğin "Benioku" dosyaları gibi belge dosyaları için kullanılabilir.
* **Derle** -dosya derleyiciye kaynak dosya olarak geçirilir.
* **İçerik** - **içerik** olarak işaretlenen bir dosya, çağırarak <xref:System.Windows.Application.GetContentStream%2A?displayProperty=nameWithType>bir akış olarak alınabilir. ASP.NET projelerinde, bu dosyalar, dağıtıldığı sırada sitenin bir parçası olarak dahil edilir.
* **Gömülü kaynak** -dosya, derlemeye gömülebilen bir kaynak olarak derleyiciye geçirilir. Derlemeden dosyayı okumak <xref:System.Reflection.Assembly.GetManifestResourceStream%2A?displayProperty=fullName> için öğesini çağırabilirsiniz.
* **AdditionalFiles** -girdi olarak C# veya Visual Basic derleyicisine geçirilen kaynak olmayan bir metin dosyası. Bu derleme eylemi, genellikle kod kalitesini doğrulamak üzere bir proje tarafından başvurulan [çözümleyiciler](../code-quality/roslyn-analyzers-overview.md) için giriş sağlamak üzere kullanılır. Daha fazla bilgi için bkz. [ek dosyaları kullanma](https://github.com/dotnet/roslyn/blob/master/docs/analyzers/Using%20Additional%20Files.md).

## <a name="see-also"></a>Ayrıca bkz.

- [C# derleyici seçenekleri](/dotnet/csharp/language-reference/compiler-options/listed-alphabetically)
- [Visual Basic derleyici seçenekleri](/dotnet/visual-basic/reference/command-line-compiler/compiler-options-listed-alphabetically)
- [Derleme eylemleri (Mac için Visual Studio)](/visualstudio/mac/build-actions)