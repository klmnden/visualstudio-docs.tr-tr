---
title: Kodlamalar ve satır sonları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
f1_keywords:
- vs.Encoding
helpviewer_keywords:
- line breaks
- encoding
- Visual Studio, encoding
- editors, line breaks
- line break characters
- Visual Studio, line break characters
ms.assetid: 8f9b3ffc-7b8d-44f4-87cb-dc29105be12d
caps.latest.revision: 12
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 88f04720610bad5064f7f9d7a43beef2410b045f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54787472"
---
# <a name="encodings-and-line-breaks"></a>Kodlamalar ve Satır Sonları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio'da kullanabileceğiniz **dosya/Gelişmiş kaydetme seçenekleri** karakterler satır sonu türünü belirlemek için ayarları istiyorsunuz. Ayrıca, aynı ayarlarla bir dosyanın kodlamasını değiştirebilirsiniz.  
  
> [!NOTE]
>  Belirli türlerdeki geliştirme ayarları varsa (Visual Basic F#, Web geliştirme) değil de görebileceğiniz **Gelişmiş kaydetme seçenekleri** menüsünde. Ayarlarınızı (örneğin genel) değiştirmek için **Araçlar / içe ve dışa aktarma ayarları**. Daha fazla bilgi için [Visual Studio'da geliştirme ayarlarını özelleştirme](http://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
 Visual Studio'da şu karakterler satır sonu yorumlanır:  
  
- CRLF: Satır başı ve satır besleme, 000 D + 000A Unicode karakterler  
  
- LF: Satır besleme, Unicode karakter 000A  
  
- NEL: Sonraki satır, Unicode karakter 0085  
  
- LS: Unicode karakter 2028 satır ayırıcı  
  
- PS: Paragraf ayırıcı, Unicode karakter 2029  
  
  Diğer uygulamalardan kopyaladığınız metin orijinal kodlama ve satır sonu karakterleri korur. Örneğin, Not Defteri'nden metni kopyalayın ve Visual Studio'da bir metin dosyasına yapıştırın, metni Not Defteri'nde olduğu aynı ayarları içerir.  
  
  Farklı satır sonu karakterleri olan bir dosyayı açtığınızda, tutarsız satır sonu karakterleri normalleştirilmeli olup olmadığını ve hangi tür seçmek için satır sonları soran bir iletişim kutusu görebilirsiniz.
