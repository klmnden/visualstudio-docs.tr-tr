---
title: Seçenekler, Metin Düzenleyici, C/C++, Biçimlendirme
ms.date: 04/30/2018
ms.prod: visual-studio-dev15
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
manager: wpickett
ms.workload:
- cplusplus
ms.openlocfilehash: 6aa4c543d19c43bd397d7d18a185a73a4bf161a6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53960754"
---
# <a name="options-text-editor-cc-formatting"></a>Seçenekler, Metin Düzenleyici, C/C++, Biçimlendirme

C veya C++ ortamında programlama yaparken Kod Düzenleyicisi'nın varsayılan davranışını değiştirmek için bu özellik sayfalarını kullanın.

[Biçimlendirme C++ özellik sayfaları](media/cpp-formatting.png)

 Bu sayfaya erişmek için **seçenekleri** iletişim kutusunda, sol bölmede, **metin düzenleyici**, genişletme **C/C++** ve ardından **biçimlendirme** .

> [!NOTE]
> Bilgisayarınız, aşağıdaki yönergelerde yer alan Visual Studio kullanıcı arabirimi öğelerinden bazıları için farklı adlar veya konumlar gösterebilir. Sahip olduğunuz Visual Studio sürümü ve kullandığınız ayarlar bu öğeleri belirler. Daha fazla bilgi için [Visual Studio IDE'yi kişiselleştirme](../../ide/personalizing-the-visual-studio-ide.md).

## <a name="general-page"></a>Genel sayfası

Bu sayfa, siz yazarken deyimleri ve blokları biçimlendirme seçeneği içerir.

**Visual Studio 2017 sürüm 15.7 ve üzeri**: Sayfa desteği için yapılandırma seçeneklerini de sahip [ClangFormat](https://clang.llvm.org/docs/ClangFormat.html) sürüm 5.0. ClangFormat, stil ve kodunuzu .clang-format veya _clang-format dosyasında yapılandırılabilir kurallar kümesi temel biçimlendirmek kolay bir yardımcı programdır.

### <a name="configuring-clangformat-options"></a>ClangFormat seçeneklerini yapılandırma

Visual Studio 2017 sürüm 15.7 ve üzeri, ClangFormat desteği varsayılan olarak etkindir. Tüm projeleriniz uygulamak için bu ortak biçimlendirme kuralları hangisinin seçebilirsiniz: LLVM, Google, Chromium, Mozilla veya WebKit. Bir özel biçim tanımını .clang-format veya _clang-format dosyası da oluşturabilirsiniz. Bir proje klasöründe böyle bir dosya varsa, Visual Studio tüm kaynak kodu dosyaları bu klasörde ve alt klasörlerinde biçimlendirmek için kullanır. 

Varsayılan olarak, Visual Studio arka planda çalıştırır clangformat.exe yazarken biçimlendirme uygular. Çağrılan biçimlendirme komutları çalıştırmak için yalnızca el ile belirtebilirsiniz **belgeyi Biçimlendir (Ctrl + K, Ctrl + D)** veya **seçimi Biçimlendir (Ctrl + K, Ctrl + F)**.


## <a name="indentation-new-lines-spacing-wrapping-pages"></a>Yeni satırlar, girinti aralığı sarmalama sayfaları

Bu sayfalar, çeşitli biçimlendirme özelleştirmeleri etkinleştirir, ancak ClangFormat etkinse, göz ardı edilir.

## <a name="see-also"></a>Ayrıca Bkz.

- [Genel, Ortam, Seçenekler İletişim Kutusu](../../ide/reference/general-environment-options-dialog-box.md)
- [IntelliSense Kullanma](../../ide/using-intellisense.md)