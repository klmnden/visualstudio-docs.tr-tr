---
title: 'Nasıl yapılır: Derleme çıktı dizinini değiştirme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- output directory, changing
ms.assetid: a8333c89-afb2-4b1d-b2e2-9146da852402
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 0d8ee4bac6f04515439f5703fe2f98546e011af4
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54777371"
---
# <a name="how-to-change-the-build-output-directory"></a>Nasıl yapılır: Derleme Çıkış Dizinini Değiştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

(Hata ayıklama, yayın veya her ikisi için) yapılandırma olarak projeniz tarafından oluşturulan çıkış konumunu belirtebilirsiniz.  
  
> [!NOTE]
>  Varsa bir **Kurulum** proje, bu makalenin sonundaki nota bakın.  
  
## <a name="changing-the-build-output-directory"></a>Derleme çıktı dizinini değiştirme  
  
#### <a name="to-change-the-build-output-directory"></a>Derleme çıkış dizinini değiştirme  
  
1.  Menü çubuğunda, **proje**, *Appname* **özellikleri**. Ayrıca'nde proje düğümüne sağ **Çözüm Gezgini** seçip **özellikleri**.  
  
2.  Visual Basic projesi varsa, seçin **derleme** sekmesi. Bir Visual C# projesi varsa, seçin **derleme** sekmesi. Bir C++ veya JavaScript projesi varsa, seçin **genel** sekmesi.  
  
3.  Yapılandırma açılan sayfanın üstünde çıktısı yapılandırmayı seçin. dosya konumu (hata ayıklama, yayın veya tümü) değiştirmek istediğiniz.  
  
     Çıkış yolu girdisini bulun (**yapı çıkış yolu** Visual Basic'te **çıkış dizinine** Visual C++ ' ta **çıkış yolu** JavaScript ve C#). Proje dizinine göre yeni bir derleme çıktı dizinini belirtin.  
  
> [!NOTE]
>  Kurulum projesinde **çıktı dosyası adını** kutusu yalnızca, proje dosyalarının konumu değil Setup.exe dosyasının konumunu değiştirir. Daha fazla bilgi için **derleme, yapılandırma özellikleri, dağıtım Proje Özellikleri iletişim kutusu**.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Derleme sayfası, Proje Tasarımcısı (C#)](../ide/reference/build-page-project-designer-csharp.md)   
 [Genel özellik sayfası (Proje)](http://msdn.microsoft.com/library/593b383c-cd0f-4dcd-ad65-9ec9b4b19c45)   
 [Derleme ve Oluşturma](../ide/compiling-and-building-in-visual-studio.md)
