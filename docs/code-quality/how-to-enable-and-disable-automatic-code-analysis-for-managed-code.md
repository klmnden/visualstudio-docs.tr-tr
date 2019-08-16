---
title: Kod analizini etkinleştirme veya devre dışı bırakma
ms.date: 10/25/2018
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: ec0a8a3f04830115d343fcef611cfbd338163395
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69551040"
---
# <a name="how-to-enable-and-disable-automatic-code-analysis-for-managed-code"></a>Nasıl yapılır: Yönetilen kod için otomatik kod analizini etkinleştirme ve devre dışı bırakma

Her bir yönetilen kod projesi derlemeden sonra çalışacak şekilde (statik) Kod analizini yapılandırabilirsiniz. Her derleme yapılandırması için, hata ayıklama ve yayın gibi farklı kod analizi özellikleri ayarlayabilirsiniz.

Bu makale, [kod Çözümleyicileri](roslyn-analyzers-overview.md)kullanılarak canlı kod analizi değil, yalnızca eski analizler için geçerlidir.

## <a name="to-enable-or-disable-automatic-code-analysis"></a>Otomatik Kod analizini etkinleştirmek veya devre dışı bırakmak için

1. **Çözüm Gezgini**, projeye sağ tıklayın ve ardından **Özellikler**' i seçin.

1. Projenin Özellikler iletişim kutusunda **Kod Analizi** sekmesini seçin.

   > [!TIP]
   > .NET Core ve .NET Standard uygulamalarında daha yeni proje türleri **Kod Analizi** sekmesine sahip değildir. Bu proje türleri için eski analiz kullanılamaz, ancak [.net Compiler platform tabanlı kod Çözümleyicileri](roslyn-analyzers-overview.md)kullanarak canlı kod analizi edinebilirsiniz. Kod Çözümleyicileri uyarılarını gizlemek için, bu makalenin sonundaki nota bakın.

1. **Yapılandırmada** derleme türünü ve hedef platformu **Platform**' da belirtin.

1. Otomatik Kod analizini etkinleştirmek veya devre dışı bırakmak için, **derlemede Kod analizini etkinleştir** onay kutusunu işaretleyin veya temizleyin.

> [!NOTE]
> **Derlemede Kod analizini etkinleştir** onay kutusu yalnızca eski Analizi etkiler. Bu, her zaman derlemede yürütülen [.net Compiler platform tabanlı kod Çözümleyicileri](roslyn-analyzers-overview.md)etkilemez. Bu, bunları bir NuGet paketi olarak yüklediyseniz derleme sırasında yürütülür. **Hata listesi**çözümleyici hatalarını temizlemek istiyorsanız, tüm geçerli ihlallerin Kod analizini **Çözümle** > ve menü çubuğunda**etkin sorunları Gizle** ' yi seçerek gizleyebilirsiniz. Daha fazla bilgi için bkz. [Ihlalleri gösterme](use-roslyn-analyzers.md#suppress-violations).
