---
title: Windows Vista'da ClickOnce dağıtımı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- UAC manifest generation
- ClickOnce deployment, Windows
- manifest generation
- Windows, ClickOnce deployment
ms.assetid: b21a0ebc-0ff6-4f49-8993-7d1ad3f8cac2
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 15af68e52a902003cd483cb6705ab4ded947f1a2
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54783552"
---
# <a name="clickonce-deployment-on-windows-vista"></a>Windows Vista'da ClickOnce Dağıtımı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio'da uygulamaları oluşturma, Windows Vista kullanıcı hesabı denetimi (UAC) normalde gömülü bir bildirim üretir uygulamanın yürütülebilir dosyasına ikili olarak XML verilerinde kodlanmış. ClickOnce ve Registration-Free COM uygulamaları harici bildirim gerektirdiğinden, Visual Studio bu tür bir gömülü bildirimi yerine UAC verilerini içeren projeler için bir dosya oluşturur. Varsayılan olarak, Visual Studio, bilgileri (ClickOnce ve Registration-Free COM dağıtım için) dış UAC bildirim bilgilerini oluşturmak ya da (tüm diğer durumlarda için) uygulamanın yürütülebilir dosyasına katıştırma app.manifest adlı bir dosyadan kullanır. Visual Studio, bildirim oluşturmak üzere aşağıdaki seçenekleri sağlar:  
  
- Gömülü bir bildirim kullanın. UAC veri uygulamanın yürütülebilir dosyasına katıştırma ve normal kullanıcı olarak çalıştırın.  
  
   (ClickOnce kullanmadığınız sürece) varsayılan ayar budur. Bu ayar, Visual Studio çalıştığı her zamanki şekilde Windows Vista'da destekleyecek; diğer bir deyişle, her iki kullanarak bir iç ve dış bildirimi nesil `AsInvoker`.  
  
- Harici bildirim kullanın. Harici bildirim app.manifest kullanarak oluşturun.  
  
   Bu, yalnızca dış bildirimi App.manifest'te yer bilgileri kullanarak oluşturur. ClickOnce veya Registration-Free COM kullanılarak bir uygulama yayımladığınızda, Visual Studio app.manifest projeye ekler ve bu seçenek ekler.  
  
- Hiçbir bildirim kullanın. Bir bildirim olmadan uygulamayı oluşturun.  
  
   Bu yaklaşım olarak da bilinir, *sanallaştırma*. Visual Studio'nun önceki sürümlerindeki mevcut uygulamalarla uyumluluk için bu seçeneği kullanın.  
  
  Yeni özellikler kullanılabilir **uygulama** sayfası Proje Tasarımcısı (Visual C# projeleri yalnızca için) ve MSBuild proje dosyası biçimi.  
  
  Visual Studio IDE içinde UAC bildirim üretme yapılandırma yöntemi (Visual C# ve Visual Basic) proje türüne göre değişebileceğini unutmayın.  
  
  Bildirim oluşturmak üzere Visual C# projelerini yapılandırma hakkında daha fazla bilgi için bkz: [uygulama sayfası, Proje Tasarımcısı (C#)](../ide/reference/application-page-project-designer-csharp.md).  
  
  Visual Basic projeleri için bildirim oluşturma yapılandırma hakkında daha fazla bilgi için bkz: [uygulama sayfası, Proje Tasarımcısı (Visual Basic)](../ide/reference/application-page-project-designer-visual-basic.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce güvenliği ve dağıtımı](../deployment/clickonce-security-and-deployment.md)   
 [Kullanıcı izinleri ve Visual Studio](http://msdn.microsoft.com/d5c55084-1e7b-4b61-b478-137db01c0fc0)   
 [Uygulama sayfası, Proje Tasarımcısı (C#)](../ide/reference/application-page-project-designer-csharp.md)   
 [Uygulama Sayfası, Proje Tasarımcısı (Visual Basic)](../ide/reference/application-page-project-designer-visual-basic.md)
