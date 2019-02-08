---
title: 'Nasıl yapılır: Derleme çıkış dizinini değiştirme'
ms.date: 11/04/2016
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
ms.openlocfilehash: 2f254c29f2951484869b814f13d1a346080fab07
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55911539"
---
# <a name="how-to-change-the-build-output-directory"></a>Nasıl yapılır: Derleme çıkış dizinini değiştirme

(Hata ayıklama, yayın veya her ikisi için) yapılandırma olarak projeniz tarafından oluşturulan çıkış konumunu belirtebilirsiniz.

> [!NOTE]
> Varsa bir **Kurulum** proje, bu makalenin sonundaki nota bakın.

## <a name="change-the-build-output-directory"></a>Derleme çıkış dizinini değiştirme

1.  Menü çubuğunda, **proje** > **\<uygulamaadı > Özellikleri**. Ayrıca'nde proje düğümüne sağ **Çözüm Gezgini** seçip **özellikleri**.

2.  Visual Basic projesi varsa, seçin **derleme** sekmesi. Bir C# projesi varsa, seçin **derleme** sekmesi. Bir C++ veya JavaScript projesi varsa, seçin **genel** sekmesi.

3.  Yapılandırma açılan sayfanın üstünde çıktısı yapılandırmayı seçin. dosya konumu (hata ayıklama, yayın veya tümü) değiştirmek istediğiniz.

     Çıkış yolu girdisini bulun (**yapı çıkış yolu** Visual Basic'te **çıkış dizinine** Visual C++ ' ta **çıkış yolu** JavaScript ve C#). Proje dizinine göre yeni bir derleme çıktı dizinini belirtin.

> [!NOTE]
> Kurulum projesinde **çıktı dosyası adını** kutusu yalnızca konumunu değiştirir *Setup.exe* dosyası, proje dosyalarının konumu değil. Daha fazla bilgi için **derleme, yapılandırma özellikleri, dağıtım Proje Özellikleri iletişim kutusu**.

## <a name="see-also"></a>Ayrıca bkz.

- [Derleme sayfası, Proje Tasarımcısı (C#)](../ide/reference/build-page-project-designer-csharp.md)
- [Genel özellik sayfası (Proje)](/cpp/ide/general-property-page-project)
- [Derleme ve oluşturma](../ide/compiling-and-building-in-visual-studio.md)