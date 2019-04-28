---
title: 'Nasıl yapılır: .NET Framework kaynağında hata ayıklama | Microsoft Docs'
ms.date: 11/19/2018
ms.topic: conceptual
helpviewer_keywords:
- debugging, .NET Framework source
ms.assetid: fc12e472-ac6a-4e77-8e22-a769e13a03b8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 25f40b0528b794863aabdb13ed9785d2b0c551b8
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62894280"
---
# <a name="how-to-debug-net-framework-source"></a>Nasıl yapılır: .NET Framework kaynağında hata ayıklama

.NET Framework kaynağında hata ayıklamak için şunları yapmalısınız:

- İçinde .NET Framework kaynak Adımlamayı etkinleştir.

- Kod için hata ayıklama erişimine sahiptir.

  Hata ayıklama simgeleri hemen karşıdan yükleyin ya da daha sonra indirme seçenekleri seçebilirsiniz. Simgeleri hemen indirmeyi yoktur, bunlar uygulamanızı hata ayıklama sonraki başlatışınızda indirirsiniz. Hata ayıklama sırasında kullanabilirsiniz **modülleri** veya **çağrı yığını** indirmek ve simgeleri yüklemek için windows.

### <a name="to-enable-stepping-into-net-framework-source"></a>.NET Framework kaynağına ilerlemesine adımlamak için

1. Altında **Araçları** (veya **hata ayıklama**) > **seçenekleri** > **hata ayıklama** > **genel**seçin **etkinleştirme .NET Framework kaynak Adımlamayı**.

   - Yalnızca kendi kodum tablonuz varsa bir uyarı iletişim kutusu, yalnızca kendi kodum şimdi devre dışı olduğunu bildirir. **Tamam**’ı seçin.

   - Ayarlanmış bir yerel sembol önbellek yoksa bir uyarı iletişim kutusu, varsayılan sembol önbelleği ayarlandığını bildirir. **Tamam**’ı seçin.

1. Seçin **Tamam** kapatmak için **seçenekleri** iletişim.

### <a name="to-set-or-change-symbol-source-locations-and-loading-behavior"></a>Ayarlamak veya sembol kaynak konumları ve yükleme davranışı değiştirmek için

1. Seçin **sembolleri** kategorisi altında **Araçları** (veya **hata ayıklama**) > **seçenekleri** > **hataayıklama**.

1. Üzerinde **sembolleri** sayfasındaki **sembol dosyası (.pdb) konumlar**seçin **Microsoft sembol sunucuları** genel Microsoft sembol sunucularından sembolleri erişim için. Diğer simge konumları eklemek ve yüklenme sırasını değiştirmek için araç çubuğu düğmeleri seçin.

1. Yerel sembol önbelleğinizi değiştirmek için düzenlemek veya altında farklı bir konuma göz atın **önbellek sembolleri bu dizinde**.

1. Simgeleri hemen karşıdan yüklemek seçin **tüm sembolleri**. Bu düğme, yalnızca hata ayıklarken kullanılabilir.

   Sembolleri şimdi karşıdan yoksa, bunlar sonraki hata ayıklama işlemi başlattığınızda indirilmesi.

1. Seçin **Tamam** kapatmak için **seçenekleri** iletişim.

### <a name="to-load-symbols-from-the-modules-or-call-stack-windows"></a>Modülleri veya çağrı yığını simgeleri yüklemek için windows

1. Hata ayıklama sırasında penceresini seçerek açın. **hata ayıklama** > **Windows** > **modülleri** (veya basın **Ctrl + Alt + U**) veya **hata ayıklama** > **Windows** > **çağrı yığını** (**Ctrl + Alt + C**).

1. Sembol yüklenmedi olmayan bir modül sağ tıklayın. İçinde **modülleri** sembol yükleme durumu penceresinde konusu **simge durumu** sütun. İçinde **çağrı yığını** penceresinde durumudur **çerçeve durumu** sütun ve çerçeve grileştirilmiş.

   - Seçin **yük sembolleri** menüsünden bulun ve sembol dosyaları bir klasörden makinenize yükleyin.

   - Seçin **sembol yükleme bilgisi** hata ayıklayıcı semboller için Aranan konumları göstermek için.

   - Seçin **sembol ayarları** açmak için **sembolleri** sayfası. Üzerinde **sembolleri** sayfasındaki **sembol dosyası (.pdb) konumlar**seçin **Microsoft sembol sunucuları** genel Microsoft sembol sunucularından sembolleri erişim için. Diğer simge konumları eklemek ve yüklenme sırasını değiştirmek için araç çubuğu düğmeleri seçin. Seçin **Tamam** iletişim kutusunu kapatmak için.

### <a name="see-also"></a>Ayrıca bkz.
- [Yönetilen kodda hata ayıklama](../debugger/debugging-managed-code.md)
- [Sembol (.pdb) ve kaynak dosyaları belirtme](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)