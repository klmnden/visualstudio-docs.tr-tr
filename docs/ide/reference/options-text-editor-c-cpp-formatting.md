---
title: Seçenekler, Metin Düzenleyici, C/C++, Biçimlendirme
ms.date: 04/30/2018
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.C/C++.Formatting.General
- VS.ToolsOptionsPages.Text_Editor.C%2fC%2b%2b.Formatting.General
dev_langs:
- CPP
helpviewer_keywords:
- Text Editor Options dialog box, formatting
- ClangFormat
ms.assetid: cb6f1cbb-5305-48da-a8e8-33fd70775d46
author: mikeblome
ms.author: mblome
manager: markl
ms.workload:
- cplusplus
ms.openlocfilehash: b866d09dbd448950a641ebb59501c13c3bf35188
ms.sourcegitcommit: 85d66dc9fea3fa49018263064876b15aeb6f9584
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/24/2019
ms.locfileid: "68461811"
---
# <a name="options-text-editor-cc-formatting"></a>Seçenekler, Metin Düzenleyici, C/C++, Biçimlendirme

C veya C++içinde programlama yaparken kod düzenleyicisinin varsayılan davranışını değiştirmek için bu özellik sayfalarını kullanın.

![C++Özellik sayfalarını biçimlendirme](media/cpp-formatting.png)

Bu sayfaya erişmek için, **Seçenekler** iletişim kutusunda, sol bölmede, **metin düzenleyici**' yi genişletin, **C++C/** öğesini genişletin ve ardından **biçimlendirme**' ye tıklayın.

> [!NOTE]
> Bilgisayarınız, aşağıdaki yönergelerde yer alan Visual Studio kullanıcı arabirimi öğelerinden bazıları için farklı adlar veya konumlar gösterebilir. Sahip olduğunuz Visual Studio sürümü ve kullandığınız ayarlar bu öğeleri belirler. Daha fazla bilgi için bkz. [Visual STUDIO IDE 'Yi kişiselleştirme](../../ide/personalizing-the-visual-studio-ide.md).

## <a name="general-page"></a>Genel sayfa

Bu sayfada, bunları yazarken ifadeleri ve blokları biçimlendirme seçenekleri bulunur.

::: moniker range="vs-2017"

**Visual Studio 2017 sürüm 15,7 ve üzeri**:

::: moniker-end

Bu sayfada [Clangformat](https://clang.llvm.org/docs/ClangFormat.html) sürüm 5,0 için destek yapılandırma seçenekleri de bulunur. ClangFormat, bir. Clang-format veya _clang-Format dosyasında yapılandırılabilecek bir dizi kurala göre kodunuzu stili ve biçimlendirmeyi kolaylaştıran bir yardımcı programdır.

### <a name="configuring-clangformat-options"></a>ClangFormat seçeneklerini yapılandırma

::: moniker range="vs-2017"

**Visual Studio 2017 sürüm 15,7 ve üzeri**:

::: moniker-end

ClangFormat desteği varsayılan olarak etkindir. Tüm projelerinize hangi ortak biçimlendirme kurallarından uygulanacağını seçebilirsiniz: LLVM, Google, Kmıum, Mozilla veya WebKit. Ayrıca, özel bir biçim tanımı da oluşturabilirsiniz. Clang-format veya _clang-Format dosyası. Bu tür bir dosya proje klasöründe mevcutsa, Visual Studio bu klasör ve alt klasörlerindeki tüm kaynak kodu dosyalarını biçimlendirmek için onu kullanır.

Varsayılan olarak, Visual Studio arka planda clangformat. exe ' yi çalıştırarak yazarken biçimlendirme uygular. Ayrıca, bunu yalnızca el ile çağrılan biçimlendirme komutları **Biçim belgesi (Ctrl + k, CTRL + D)** veya **Biçim seçimi (Ctrl + k, CTRL + F)** için çalıştırmayı belirtebilirsiniz.

## <a name="indentation-new-lines-spacing-wrapping-pages"></a>Girintileme, yeni satırlar, Aralık kaydırma sayfaları

Bu sayfalar, çeşitli biçimlendirme özelleştirmelerini etkinleştirir ancak ClangFormat etkinse yok sayılır.

## <a name="see-also"></a>Ayrıca bkz.

- [Genel, Ortam, Seçenekler İletişim Kutusu](../../ide/reference/general-environment-options-dialog-box.md)
- [IntelliSense Kullanma](../../ide/using-intellisense.md)