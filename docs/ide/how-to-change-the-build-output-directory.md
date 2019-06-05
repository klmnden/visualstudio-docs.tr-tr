---
title: 'Nasıl yapılır: Derleme çıkış dizinini değiştirme'
ms.date: 05/15/2019
ms.technology: vs-ide-compile
ms.topic: conceptual
helpviewer_keywords:
- output directory, changing
ms.assetid: a8333c89-afb2-4b1d-b2e2-9146da852402
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f9dce876b477dfb802b9cf64214af2ca1cec6a4e
ms.sourcegitcommit: 5483e399f14fb01f528b3b194474778fd6f59fa6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/05/2019
ms.locfileid: "66715362"
---
# <a name="how-to-change-the-build-output-directory"></a>Nasıl yapılır: Derleme çıkış dizinini değiştirme

(Hata ayıklama, yayın veya her ikisi için) yapılandırma başına temelinde projeniz tarafından oluşturulan çıkış konumunu belirtebilirsiniz.

## <a name="change-the-build-output-directory"></a>Derleme çıkış dizinini değiştirme

1. Projenin özellik sayfalarındaki açmak için ' nde proje düğümüne sağ **Çözüm Gezgini** seçip **özellikleri**.

2. Proje türüne göre uygun sekmeyi seçin:

   - İçin C#seçin **derleme** sekmesi.
   - Visual Basic için seçin **derleme** sekmesi.
   - İçin C++ veya JavaScript seçin **genel** sekmesi.

3. Yapılandırma açılan sayfanın üstünde çıktısı yapılandırmayı seçin. dosya değiştirmek istediğiniz konumu (**hata ayıklama**, **yayın**, veya **yapılandırmalarında**).

4. Çıkış yolu giriş sayfasında bulma&mdash;, proje türüne bağlı olarak değişir:

   - **Çıkış yolu** için C# ve JavaScript projeleri
   - **Yapı çıkış yolu** Visual Basic projeleri
   - **Çıkış dizini** görsel için C++ projeleri

   Çıkış (mutlak veya göreli proje kök dizinine) oluşturun veya seçin, türü yolunda **Gözat** bunun yerine bu klasöre gidin.

   ![Path özelliği için bir Visual Studio çıktı C# proje](media/output-path.png)

> [!TIP]
> Çıktı, belirttiğiniz konuma oluşturulmadıysa, karşılık gelen yapılandırma oluşturmakta olduğunuza emin olun (örneğin, **hata ayıklama** veya **yayın**) menü çubuğunda seçerek Visual Studio.
>
> ![Visual Studio 2019 seçicide yapılandırma derleme](media/build-configuration-chooser.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Derleme sayfası, Proje Tasarımcısı (C#)](../ide/reference/build-page-project-designer-csharp.md)
- [Genel özellik sayfası (Proje)](/cpp/build/reference/general-property-page-project)
- [Derleme ve oluşturma](../ide/compiling-and-building-in-visual-studio.md)