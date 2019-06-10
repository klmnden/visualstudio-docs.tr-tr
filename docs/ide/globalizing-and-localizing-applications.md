---
title: Yerelleştirme araçları
ms.date: 02/15/2019
ms.topic: reference
helpviewer_keywords:
- globalization [Visual Studio]
- Visual Basic code, international applications
- C#, international applications
- localization [Visual Studio]
- world-ready applications
- international applications [Visual Studio]
ms.assetid: 4d9815ae-3e80-4b4d-933d-f8309aee18d5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 934427c2bfba769968b7aeb364625b71af47eca7
ms.sourcegitcommit: 51dad3e11d7580567673e0d426ab3b0a17584319
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/10/2019
ms.locfileid: "66820876"
---
# <a name="develop-globalized-and-localized-apps"></a>Genelleştirilmiş ve yerelleştirilmiş uygulamalar geliştirin

Visual Studio yapar yerleşik hizmetlerinin avantajlarından yararlanarak uluslararası bir hedef kitle için kolay geliştirme [.NET](/dotnet/standard/globalization-localization/).

Örneğin, proje sistemi Windows Forms uygulamaları için geri dönüş UI kültürü hem de her ek UI kültürü için kaynak dosyaları oluşturabilirsiniz. Visual Studio'da bir proje oluşturduğunuzda, kaynak dosyalarını Visual Studio XML biçimi (.resx) Ara bir ikili biçimine (.resources), ardından uydu derlemeleri içinde gömülü derlenir. Daha fazla bilgi için [Visual Studio'daki kaynak dosyaları](/dotnet/framework/resources/creating-resource-files-for-desktop-apps#VSResFiles) ve [Masaüstü uygulamaları için uydu derlemeleri oluşturma](/dotnet/framework/resources/creating-satellite-assemblies-for-desktop-apps).

## <a name="bidirectional-languages"></a>Çift yönlü diller

Sağ-Arapça ve İbranice gibi sola doğru dillerde yazılan metin görüntüleyen uygulamalar oluşturmak için Visual Studio kullanabilirsiniz. Bazı özellikler için özellikleri ayarlayabilirsiniz. Diğer durumlarda, kod özellikleri uygulamalıdır.

> [!NOTE]
> Girin ve çift yönlü diller görüntülemek için uygun dili ile yapılandırılmış bir Windows sürümü ile çalışmalısınız. Bu bir İngilizce sürümüyle ilgili dil paketi yüklü olan Windows veya Windows uygun şekilde yerelleştirilmiş sürümünü olabilir.

### <a name="apps-that-support-bidirectional-languages"></a>Çift yönlü diller destekleyen uygulamalar

- Windows uygulamaları

   Tam olarak iki yönlü metnin sağdan sola okuma düzeni ve yansıtma (windows, menüler, iletişim kutuları ve benzeri düzenini ters) için destek içeren çift yönlü uygulamalar oluşturabilirsiniz. Yansıtma dışında bu özellikler varsayılan olarak veya özellik ayarları olarak kullanılabilir. Yansıtma ileti kutuları gibi bazı özellikler için doğal olarak desteklenir. Ancak, diğer durumlarda kod yansıtma uygulamalıdır. Daha fazla bilgi için [Windows Forms uygulamaları için çift yönlü destek](/dotnet/framework/winforms/advanced/bi-directional-support-for-windows-forms-applications).

- Web uygulamaları

   Web Hizmetleri, UTF-8 ve çift yönlü diller gerektiren uygulamalar için uygun hale getirir, Unicode metni gönderip destekler. Web istemcisi uygulamalarını tarayıcılar için kullanıcı arabirimini kullanır, çift yönlü derecesini, destek için bir web uygulaması kullanıcı tarayıcısı bu çift yönlü Özellikler ne kadar iyi destekleyen bağlıdır. Visual Studio'da, Arapça veya İbranice metin, sağdan sola okuma düzeni, dosya kodlamasını ve yerel kültür ayarları için desteğe sahip uygulamalar oluşturabilirsiniz. Daha fazla bilgi için [ASP.NET web uygulamaları için çift yönlü destek](https://msdn.microsoft.com/Library/5576f9b1-9b86-41ef-8354-092d366bcd03).

> [!NOTE]
> Konsol uygulamaları, metin çift yönlü dil desteği içermez. Windows konsol uygulamaları ile nasıl çalıştığına ilişkin bir sonucu budur.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da çift yönlü dil desteği](use-bidirectional-languages.md)
- [Globalize ve .NET uygulamalarını yerelleştirme](/dotnet/standard/globalization-localization/)
- [.NET uygulamalarında kaynakları](/dotnet/framework/resources/)