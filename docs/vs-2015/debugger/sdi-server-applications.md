---
title: SDI sunucu uygulamaları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- SDI server applications
- SDI server applications, debugging
ms.assetid: 09713718-1376-4753-b119-26f36639693e
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 1296c0f43d0409df0081861095c5ec068932bbc1
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54777618"
---
# <a name="sdi-server-applications"></a>SDI Sunucu Uygulamaları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir SDI sunucu uygulaması hata ayıklaması yaptığınız varsa, belirtmeniz gerekir `/Embedding` veya `/Automation` içinde **komut satırı bağımsız değişkenleri** özelliğinde *proje* özellik sayfaları iletişim kutusu için C/C++, C#, veya Visual Basic projeleri.  
  
 Bu komut satırı bağımsız değişkenleri ile onu başlatan bir kapsayıcıdan artırmadığı hata ayıklayıcı sunucu uygulaması başlatabilirsiniz. Program Yöneticisi'nden veya Dosya Yöneticisi kapsayıcıyı başlangıç hata ayıklayıcıda çalışmaya server örneğini kullanmak için kapsayıcısını neden olur.  
  
## <a name="finding-the-command-line-arguments-property"></a>Komut satırı bağımsız değişkenleri özelliğini bulma  
 Erişim için *proje* özellik sayfaları iletişim kutusu, Çözüm Gezgini'nde projenize sağ tıklayın ve kısayol menüsünden Özellikler'i seçin. Komut satırı bağımsız değişkenleri özelliğini bulmak için yapılandırma özellikleri kategoriyi genişletmek ve hata ayıklama Sayfası'nı tıklatın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [COM ve ActiveX hata ayıklaması](../debugger/com-and-activex-debugging.md)   
 [Nasıl yapılır: COM Sunucularında Hata Ayıklama](../debugger/how-to-debug-com-servers.md)
