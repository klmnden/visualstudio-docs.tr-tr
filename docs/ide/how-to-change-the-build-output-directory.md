---
title: 'Nasıl yapılır: Derleme çıkış dizinini değiştirme'
ms.date: 05/15/2019
ms.technology: vs-ide-compile
ms.topic: conceptual
helpviewer_keywords:
- output directory, changing
ms.assetid: a8333c89-afb2-4b1d-b2e2-9146da852402
author: ghogen
ms.author: ghogen
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e006be2099d5132ce7445f1e8fe74b0f2752c260
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68416789"
---
# <a name="how-to-change-the-build-output-directory"></a>Nasıl yapılır: Derleme çıkış dizinini değiştirme

Projeniz tarafından oluşturulan çıktının yapılandırma bazında (hata ayıklama, yayın veya her ikisi için) konumunu belirtebilirsiniz.

## <a name="change-the-build-output-directory"></a>Derleme çıkış dizinini değiştirme

1. Projenin özellik sayfalarını açmak için **Çözüm Gezgini** içindeki proje düğümüne sağ tıklayın ve **Özellikler**' i seçin.

2. Proje türüne göre uygun sekmeyi seçin:

   - İçin C#, **derleme** sekmesini seçin.
   - Visual Basic için **Derle** sekmesini seçin.
   - Veya C++ JavaScript için **genel** sekmesini seçin.

3. Üstteki yapılandırma açılır penceresinde çıkış dosyası konumunu değiştirmek istediğiniz yapılandırmayı (**hata ayıklama**, **yayın**veya **tüm yapılandırmalar**) seçin.

4. Proje türüne göre farklılık gösteren sayfada&mdash;çıkış yolu girişini bulun:

   - Ve JavaScript projeleri C# için **çıkış yolu**
   - Visual Basic projeleri için **derleme çıkış yolu**
   - Görsel C++ projeler için **çıkış dizini**

   Çıkış oluşturmak için yolu yazın (kök proje dizinine mutlak veya göreli) veya bunun yerine bu klasöre gitmek için **Gözden** geçirme ' yi seçin.

   ![Visual Studio C# projesi için çıkış yolu özelliği](media/output-path.png)

> [!TIP]
> Çıktı belirttiğiniz konuma oluşturulmadığından, Visual Studio menü çubuğunda ilgili yapılandırmayı (örneğin, **hata ayıklama** veya **Sürüm**) oluştururken emin olun.
>
> ![Visual Studio 2019 ' de derleme yapılandırma Seçicisi](media/build-configuration-chooser.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Derleme sayfası, proje Tasarımcısı (C#)](../ide/reference/build-page-project-designer-csharp.md)
- [Genel özellik sayfası (proje)](/cpp/build/reference/general-property-page-project)
- [Derleme ve oluşturma](../ide/compiling-and-building-in-visual-studio.md)