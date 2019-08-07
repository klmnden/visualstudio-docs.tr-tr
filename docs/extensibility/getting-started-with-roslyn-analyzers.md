---
title: Roslyn çözümleyicilerine Başlarken | Microsoft Docs
ms.date: 04/02/2018
ms.topic: conceptual
ms.assetid: 367c2ec8-3059-46a5-9d1c-57bead0419e7
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 21b2d77d8c038988fa77293280c9ff7ad38cc82e
ms.sourcegitcommit: 90c3187d804ad7544367829d07ed4b47d3f8a72d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2019
ms.locfileid: "68822336"
---
# <a name="get-started-with-roslyn-analyzers"></a>Roslyn Çözümleyicileri ile çalışmaya başlama

Visual Studio 'da canlı, proje tabanlı kod Çözümleyicileri sayesinde, API yazarları, NuGet paketlerinin bir parçası olarak etki alanına özgü kod analizini sevk edebilir. Bu çözümleyiciler .NET Compiler Platform (kod-adı "Roslyn") tarafından korunduğundan, satırı bitirmeden (sorunları çözmek için kodunuzu derlemek için daha fazla beklememeniz gerekmez) kodunuzda uyarı üretebilirler. Çözümleyiciler, kodunuzu hemen temizleyebilmeniz için Visual Studio ampul istemiyle otomatik bir kod düzeltmesini de yüzeylere açabilir.

## <a name="get-started"></a>Kullanmaya başlayın

[Roslyn çözümleyicilerine genel bakış](../code-quality/roslyn-analyzers-overview.md)

[Öğretici: İlk çözümleyicinizi ve kod düzeltmesini yazın](/dotnet/csharp/roslyn-sdk/tutorials/how-to-write-csharp-analyzer-code-fix)

[Kod düzeltmeleri Ekle Izlenecek yol: Kullanıcılara çözümleyici sorunları için düzeltmeler sağlama](https://msdn.microsoft.com/magazine/dn904670.aspx)

[Gerçek dünya Roslyn Çözümleyicisi](../extensibility/roslyn-analyzers-and-code-aware-library-for-immutablearrays.md) ve ayrıca [konuşabilirsiniz](https://channel9.msdn.com/events/Build/2015/3-725)

[GitHub 'daki birkaç örnek, üç tür çözümleyiciler halinde gruplandırılır](https://github.com/dotnet/roslyn/blob/master/docs/analyzers/Analyzer%20Samples.md)

## <a name="see-also"></a>Ayrıca bkz.

- [.NET derleyicisi platform paketi sürüm başvurusu](roslyn-version-support.md)
- [GitHub OSS sitesinde daha fazla belge](https://github.com/dotnet/roslyn/tree/master/docs/analyzers)
- [Roslyn Çözümleyicileri ile uygulanan FxCop kuralları](../code-quality/fxcop-rule-port-status.md)
