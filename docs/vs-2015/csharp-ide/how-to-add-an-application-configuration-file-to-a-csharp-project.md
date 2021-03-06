---
title: 'Nasıl yapılır: Bir uygulama yapılandırma dosyasına ekleyin bir C# proje | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
dev_langs:
- CSharp
helpviewer_keywords:
- app.config files, adding to C# projects
ms.assetid: 9caf6bb0-c2fc-4ab6-ba69-bed3b880fbf8
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: bc5c8dbad4d2bb248a3183e2e73d7c2932e7bce4
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65681721"
---
# <a name="how-to-add-an-application-configuration-file-to-a-c-project"></a>Nasıl yapılır: Bir uygulama yapılandırma dosyasına ekleyin bir C# proje
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir C# projesine uygulama yapılandırma dosyası (app.config dosyası) ekleyerek, ortak dil çalışma zamanının nasıl bulur ve derleme dosyalarını yükler özelleştirebilirsiniz. Uygulama yapılandırma dosyaları hakkında daha fazla bilgi için bkz. [çalışma zamanı derlemeleri nasıl konumlandırır](https://msdn.microsoft.com/library/772ac6f4-64d2-4cfb-92fd-58096dcd6c34).  
  
> [!NOTE]
> Windows Store desteklemiyor <xref:System.Configuration>. Sonuç olarak, Store uygulamaları, bir app.config şablonunu içermez.  
  
 Projenizi yapılandırdığınızda, geliştirme ortamı, app.config dosyasına otomatik olarak kopyalar, yürütülebilir dosyanın eşleştirilecek kopyalama dosya adını değiştirir ve ardından kopya ait bin dizinine taşır.  
  
### <a name="to-add-an-application-configuration-file-to-your-c-project"></a>C# projenize bir uygulama yapılandırma dosyası eklemek için  
  
1. Menü çubuğunda, **proje**, **Yeni Öğe Ekle**.  
  
     **Yeni Öğe Ekle** iletişim kutusu görünür.  
  
2. Genişletin **yüklü**, genişletme **Visual C# öğeleri**ve ardından **uygulama yapılandırma dosyası** şablonu.  
  
3. İçinde **adı** metin kutusuna bir ad girin ve ardından **Ekle** düğmesi.  
  
     App.config adlı bir dosyayı projenize eklenir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uygulama ayarları (.NET) yönetme](../ide/managing-application-settings-dotnet.md)   
 [Yapılandırma dosyası şeması](https://msdn.microsoft.com/library/69003d39-dc8a-460c-a6be-e6d93e690b38)   
 [Uygulamaları yapılandırma](https://msdn.microsoft.com/library/86bd26d3-737e-4484-9782-19b17f34cd1f)   
 [Nasıl yapılır: Bir uygulamayı .NET Framework sürümünü hedefleyecek şekilde yapılandırma](https://msdn.microsoft.com/5247b307-89ca-417b-8dd0-e8f9bd2f4717)   
 [C# için Visual Studio Geliştirme Ortamını Kullanma](../csharp-ide/using-the-visual-studio-development-environment-for-csharp.md)