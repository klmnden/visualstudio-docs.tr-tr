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
ms.openlocfilehash: b0fda2363ec63572f29c6687cc10ee9a7ee06c76
ms.sourcegitcommit: 283f2dbce044a18e9f6ac6398f6fc78e074ec1ed
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/16/2019
ms.locfileid: "65805045"
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
- [Genel özellik sayfası (Proje)](/cpp/ide/general-property-page-project)
- [Derleme ve oluşturma](../ide/compiling-and-building-in-visual-studio.md)