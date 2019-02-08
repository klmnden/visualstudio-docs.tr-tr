---
title: Etkinleştirmek veya devre dışı kod analizi
ms.date: 10/25/2018
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 4878c25021d87e91f6a575d11a876d7aac2455d5
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55918136"
---
# <a name="how-to-enable-and-disable-automatic-code-analysis-for-managed-code"></a>Nasıl yapılır: Enable ve disable yönetilen kod için otomatik kod analizi

(Statik) kod analizi, yönetilen kod projesi, her yapıdan sonra çalıştırmak için yapılandırabilirsiniz. Farklı kod analizi özelliklerini her derleme yapılandırması ayarlayın, örneğin, hata ayıklama ve yayın.

Bu makale yalnızca statik kod analizi ve değil Canlı kod analizi kullanarak geçerlidir [Roslyn kod Çözümleyicileri](roslyn-analyzers-overview.md).

## <a name="to-enable-or-disable-automatic-code-analysis"></a>Etkinleştirme veya devre dışı otomatik kod çözümlemesini

1. İçinde **Çözüm Gezgini**, projeye sağ tıklayın ve ardından **özellikleri**.

1. Proje Özellikleri iletişim kutusunda seçin **Kod Analizi** sekmesi.

   > [!TIP]
   > Yeni proje türleri gibi .NET Core ve .NET Standard uygulamalara sahip bir **Kod Analizi** sekmesi. Statik kod analizi için bu proje türleri kullanılabilir değildir, ancak hala canlı Kod Analizi kullanarak alabilirsiniz [Roslyn kod Çözümleyicileri](roslyn-analyzers-overview.md). Roslyn kod Çözümleyicileri gelen uyarıları bastırmak için bu makalenin sonundaki nota bakın.

1. İçinde derleme türünü belirtmeniz **yapılandırma** ve hedef platform **Platform**.

1. Etkinleştirmek veya otomatik kod analizini devre dışı bırakmak için seçin veya temizleyin **derlemede kod analizini etkinleştir** onay kutusu.

> [!NOTE]
> **Derlemede kod analizini etkinleştir** onay kutusu yalnızca statik kod analizi etkiler. Bu etkilemez [Roslyn kod Çözümleyicileri](roslyn-analyzers-overview.md), bir NuGet paketi olarak yüklü değilse derleme sırasında her zaman yürütün. Çözümleyici hataları temizlemek istiyorsanız **hata listesi**, seçerek geçerli tüm ihlalleri gizleyebilirsiniz **Çözümle** > **kod analizini Çalıştır ve etkin gösterme Sorunları** menü çubuğundaki. Daha fazla bilgi için [ihlallerini gösterme](use-roslyn-analyzers.md#suppress-violations).
