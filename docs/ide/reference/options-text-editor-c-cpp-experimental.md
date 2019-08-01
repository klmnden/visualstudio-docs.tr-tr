---
title: Seçenekler, Metin Düzenleyici, C/C++, Deneysel
ms.date: 08/02/2017
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.C/C++.Experimental
- VS.ToolsOptionsPages.Text_Editor.C%2FC%2B%2B.Experimental
- VS.ToolsOptionsPages.Text_Editor.C\C++.Experimental
author: mikeblome
ms.author: mblome
manager: markl
ms.workload:
- cplusplus
ms.openlocfilehash: 75f36d66ea46e7a0474c3b76ae000f745337fc45
ms.sourcegitcommit: 85d66dc9fea3fa49018263064876b15aeb6f9584
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/24/2019
ms.locfileid: "68461379"
---
# <a name="options-text-editor-cc-experimental"></a>Seçenekler, Metin Düzenleyici, C/C++, Deneysel

Bu seçenekleri değiştirerek, C veya C++' de programlarken IntelliSense ve gözatma veritabanı ile ilgili davranışı değiştirebilirsiniz. Bu özellikler gerçekten deneysel bir sürümündedir ve daha sonraki bir sürümde Visual Studio 'dan değiştirilebilir veya kaldırılabilir.

::: moniker range="vs-2017"

Bu makalede, Visual Studio 2017 seçenekleri açıklanmaktadır. Visual Studio 2015 için içindekiler tablosunun üzerindeki seçicide **2015** ' i seçin.

::: moniker-end

Bu özellik sayfasına erişmek için **CTRL**+**Q** tuşlarına basarak arama kutusunu etkinleştirin ve **deneysel**yazın. Arama, ilk birkaç harften sonra sayfayı bulur. Ayrıca, **Araçlar** > **Seçenekler** ' i ve **metin düzenleyicisini**genişleterek, ardından **C/C++** ve sonra **deneysel**' u seçerek buna de ulaşabilirsiniz.

Bu özellikler, Visual Studio yüklemesinde mevcuttur.

> [!NOTE]
> Bilgisayarınız, aşağıdaki yönergelerde yer alan Visual Studio kullanıcı arabirimi öğelerinden bazıları için farklı adlar veya konumlar gösterebilir. Sahip olduğunuz Visual Studio sürümü ve kullandığınız ayarlar bu öğeleri belirler. Bkz. [Visual STUDIO IDE 'Yi kişiselleştirme](../../ide/personalizing-the-visual-studio-ide.md).

## <a name="enable-predictive-intellisense"></a>Tahmine dayalı IntelliSense 'i etkinleştir

Tahmine dayalı IntelliSense, yalnızca bağlamla ilgili sonuçları görmeniz için IntelliSense açılan listesinde görüntülenen sonuçların sayısını sınırlar. Örneğin, IntelliSense açılan listesini yazıp `int x =` çağırdığınızda yalnızca tamsayılar döndüren tamsayılar veya işlevler görürsünüz. Tahmine dayalı IntelliSense varsayılan olarak kapalıdır.

::: moniker range="vs-2017"

## <a name="enable-faster-project-load"></a>Daha hızlı proje yüklemeyi etkinleştir

Visual Studio 2017 sürüm 15,3 itibariyle, bu özellik **Proje önbelleğe almayı etkinleştir** olarak adlandırılır ve [VC + + proje ayarları](vcpp-project-settings-projects-and-solutions-options-dialog-box.md) Özellik sayfasına taşınır.

Bu seçenek, Visual Studio 'Nun proje verilerini önbelleğe almasını sağlar, böylece projeyi bir sonraki açışınızda proje dosyalarından yeniden bilgi işlem yerine önbelleğe alınmış verileri yükleyebilir. Önbelleğe alınmış verilerin kullanılması, proje yükleme süresini önemli ölçüde hızlandırabilir.

::: moniker-end

## <a name="additional-features-in-the-visual-studio-marketplace"></a>Visual Studio Market ek özellikler

[Visual Studio Market](https://marketplace.visualstudio.com/search?target=VS&category=Tools&vsVersion=&subCategory=All&sortBy=Downloads)ek metin Düzenleyicisi özelliklerine gidebilirsiniz. Bir örnek, aşağıdakileri destekleyen [ C++ hızlı düzeltmelerde](https://marketplace.visualstudio.com/items?itemName=VisualCppDevLabs.CQuickFixes2017)verilmiştir:

- **Eksik #include Ekle** -kodunuzda bilinmeyen semboller için ilgili #include önerilir

- Önceki öğe gibi **ad alanı/tam niteleme simgesini kullanarak ekleme** , ancak ad alanları için

- **Eksik noktalı virgül Ekle**

- **Çevrimiçi yardım** -hata iletileriniz için çevrimiçi Yardım ara

- ve daha fazlası...

## <a name="see-also"></a>Ayrıca bkz.

- [Dile Özgü Düzenleyici Seçeneklerini Ayarlama](../../ide/reference/setting-language-specific-editor-options.md)
- [İçinde C++ yeniden düzenleme (VC blogu)](https://devblogs.microsoft.com/cppblog/all-about-c-refactoring-in-visual-studio-2015-preview/
)
