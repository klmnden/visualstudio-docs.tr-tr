---
title: Roslyn Çözümleyicileriyle çalışmaya başlama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
ms.assetid: 367c2ec8-3059-46a5-9d1c-57bead0419e7
caps.latest.revision: 7
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 104e3a30589f5892c1440266afd7917486d704ec
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62546657"
---
# <a name="getting-started-with-roslyn-analyzers"></a>Roslyn Çözümleyicileriyle Çalışmaya Başlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio'da canlı, proje temelli kod çözümleyicileriyle API yazarlar, etki alanına özgü kod analizi NuGet paketlerinin bir parçası olarak gönderebilirsiniz.  Bu Çözümleyicileri .NET derleyici Platformu (eskiden "Roslyn") tarafından desteklenen çünkü (daha fazla sorunları bulmak için kodunuzu derlemek için bekleniyor) satırı bitirdikten sonra bile önce yazdığınız sırada bunlar kodunuzdaki uyarılar oluşturabilir.  Çözümleyicileri de temiz kodunuzu oluşturan hemen izin vermek için Visual Studio ampul istemi üzerinden bir otomatik kod düzeltme ortaya çıkabilir

## <a name="getting-started"></a>Başlarken
[Roslyn Canlı kod Çözümleyicileri giriş ve gözden geçirme](https://msdn.microsoft.com/magazine/dn879356.aspx)

[Kod ekleme, izlenecek giderir: Kullanıcılar düzeltmeleri Çözümleyicisi sorunlarda sağlayabilir.](https://msdn.microsoft.com/magazine/dn904670.aspx)

[Giriş ve gerçek dünya Çözümleyicisi konuşma ilişkin kılavuz](http://channel9.msdn.com/events/Build/2015/3-725)

[Gerçek dünya Roslyn Çözümleyicinizi](../extensibility/roslyn-analyzers-and-code-aware-library-for-immutablearrays.md) olarak izleyebileceğiniz bir [konuşun](http://channel9.msdn.com/events/Build/2015/3-725)

[Üç tür Çözümleyicileri gruplandırılmış github'da çeşitli örnekleri](https://github.com/dotnet/roslyn/blob/master/docs/analyzers/Analyzer%20Samples.md)

[Giriş ve birkaç Çözümleyicileri turu](http://channel9.msdn.com/Events/dotnetConf/2015/NET-Compiler-Platform-Roslyn-Analyzers-and-the-Rise-of-Code-Aware-Libraries)

## <a name="other-resources"></a>Diğer Kaynaklar
[GitHub OSS sitesinde daha fazla belgeleri](https://github.com/dotnet/roslyn/tree/master/docs/analyzers)

[Roslyn çözümleyicilerini github'da ile uygulanan FxCop kuralı](https://github.com/dotnet/roslyn/tree/master/src/Diagnostics/FxCop)
