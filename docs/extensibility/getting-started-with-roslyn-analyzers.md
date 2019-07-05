---
title: Roslyn Çözümleyicileriyle çalışmaya başlama | Microsoft Docs
ms.date: 04/02/2018
ms.topic: conceptual
ms.assetid: 367c2ec8-3059-46a5-9d1c-57bead0419e7
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d6a6f4123f72afd8c310e627a9da6759f4c4548a
ms.sourcegitcommit: 32144a09ed46e7223ef7dcab647a9f73afa2dd55
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/05/2019
ms.locfileid: "67586963"
---
# <a name="get-started-with-roslyn-analyzers"></a>Roslyn çözümleyicileriyle çalışmaya başlama

Visual Studio'da canlı, proje temelli kod çözümleyicileriyle API yazarlar, etki alanına özgü kod analizi NuGet paketlerinin bir parçası olarak gönderebilirsiniz. Bu Çözümleyicileri .NET derleyici Platformu (eskiden "Roslyn") tarafından desteklenen çünkü (daha fazla sorunları bulmak için kodunuzu derlemek için bekleniyor) satırı bitirdikten sonra bile önce yazdığınız sırada bunlar kodunuzdaki uyarılar oluşturabilir. Çözümleyiciler, ayrıca bir otomatik kod düzeltme temiz kodunuzu oluşturan hemen izin vermek için Visual Studio ampul istemi üzerinden ortaya çıkabilir.

## <a name="get-started"></a>Kullanmaya başlayın

[Roslyn Çözümleyicileri genel bakış](../code-quality/roslyn-analyzers-overview.md)

[Öğretici: İlk Çözümleyicisi ve kod düzeltmenizi yazın](/dotnet/csharp/roslyn-sdk/tutorials/how-to-write-csharp-analyzer-code-fix)

[İzlenecek yol kod düzeltmeleri ekleyin: Kullanıcılar düzeltmeleri Çözümleyicisi sorunlarda sağlayabilir.](https://msdn.microsoft.com/magazine/dn904670.aspx)

[Gerçek dünya Roslyn çözümleyicinizi](../extensibility/roslyn-analyzers-and-code-aware-library-for-immutablearrays.md) olarak izleyebileceğiniz bir [konuşun](https://channel9.msdn.com/events/Build/2015/3-725)

[Üç tür Çözümleyicileri gruplandırılmış github'da çeşitli örnekleri](https://github.com/dotnet/roslyn/blob/master/docs/analyzers/Analyzer%20Samples.md)

## <a name="see-also"></a>Ayrıca bkz.

- [.NET derleyici platformu Paket sürümü başvurusu](roslyn-version-support.md)
- [GitHub OSS sitesinde daha fazla belgeleri](https://github.com/dotnet/roslyn/tree/master/docs/analyzers)
- [Roslyn çözümleyicileriyle uygulandığı FxCop kuralı](http://roslynanalyzersstatus.azurewebsites.net/)
