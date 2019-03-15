---
title: Roslyn çözümleyicilerini yükleme
ms.date: 08/03/2018
ms.topic: conceptual
helpviewer_keywords:
- code analysis, managed code
- analyzers
- Roslyn analyzers
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 2b1859d422b0f3a76947a64e754521efcda46e65
ms.sourcegitcommit: 4ffb7be5384ad566ce46538032bf8561754c61a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2019
ms.locfileid: "57982941"
---
# <a name="install-net-compiler-platform-analyzers"></a>.NET derleyici platformu çözümleyicilerini yükleme

Visual Studio .NET derleyici platformu çekirdek kümesini içerir (*Roslyn*) çözümleyici. Bu çözümleyici her zaman açıktır. NuGet paketleri olarak veya Visual Studio uzantıları olarak ek Çözümleyicileri yükleyebileceğiniz *VSIX* dosyaları.

## <a name="to-install-nuget-analyzer-packages"></a>NuGet Çözümleyicisi paketleri yüklemek için

1. Üzerinde www.nuget.org yüklemek istediğiniz Çözümleyicisi paket bulun. Örneğin, isteyebileceğiniz [Microsoft FxCop Çözümleyicileri yükleme](install-fxcop-analyzers.md#to-install-fxcop-analyzers-as-a-nuget-package) kodunuzu diğerlerinin yanı sıra güvenlik ve performans sorunları için denetlenecek.

2. Visual Studio kullanarak kullanarak paketi yükleyin [Paket Yöneticisi Konsolu](/nuget/quickstart/install-and-use-a-package-in-visual-studio#package-manager-console) veya [Paket Yöneticisi UI](/nuget/quickstart/install-and-use-a-package-in-visual-studio#package-manager-console).

   > [!NOTE]
   > Her bir çözümleyici paket www.nuget.org sayfa yapıştırmak için komutu gösterir **Paket Yöneticisi Konsolu**. Metni panoya kopyalamak için kullanışlı bir düğme bile yoktur.
   >
   > ![NuGet.org sayfasında Paket Yöneticisi Konsolu komut gösteriliyor](media/nuget-install-command.png)

   Çözümleyici bütünleştirilmiş kodlarının yüklenir ve görünür **Çözüm Gezgini** altında **başvuruları** > **Çözümleyicileri**.

## <a name="to-install-vsix-analyzers"></a>VSIX Çözümleyicileri yüklemek için

::: moniker range="vs-2017"

1. Visual Studio'da **Araçları** > **Uzantılar ve güncelleştirmeler**.

   **Uzantılar ve güncelleştirmeler** iletişim kutusu açılır.

   > [!NOTE]
   > Alternatif olarak, bulmak ve doğrudan Çözümleyicisi uzantısını indirin [Visual Studio Market](https://marketplace.visualstudio.com).

::: moniker-end

::: moniker range=">=vs-2019"

1. Visual Studio'da **uzantıları** > **uzantıları yönetme**.

   **Uzantıları yönetme** iletişim kutusu açılır.

   > [!NOTE]
   > Alternatif olarak, bulmak ve doğrudan Çözümleyicisi uzantısını indirin [Visual Studio Market](https://marketplace.visualstudio.com).

::: moniker-end

2. Genişletin **çevrimiçi** sol bölmesi ve ardından **Visual Studio Market**.

3. Arama kutusuna, yüklemek istediğiniz Çözümleyicisi uzantısının adını yazın. Örneğin, isteyebileceğiniz [Microsoft FxCop Çözümleyicileri yükleme](install-fxcop-analyzers.md#to-install-fxcop-analyzers-as-a-vsix) kodunuzu diğerlerinin yanı sıra güvenlik ve performans sorunları için denetlenecek.

4. Seçin **indirme**.

   Uzantı yüklenir.

5. Seçin **Tamam** iletişim kutusunu kapatın ve ardından başlatmak için Visual Studio'nun tüm örneklerini kapatın **VSIX yükleyicisi**.

   **VSIX yükleyicisi** iletişim kutusu açılır.

   ![Microsoft Kod Analizi için VSIX yükleyicisi](media/vsix-installer-code-analysis.png)

6. Seçin **Değiştir** yüklemeyi başlatmak için.

7. Bir veya iki dakika sonra yükleme işlemini tamamlar. Seçin **Kapat**.

8. Visual Studio'yu yeniden açın.

::: moniker range="vs-2017"

Seçeneğini yüklü olup olmadığını ' uzantısı denetlemek istiyorsanız **Araçları** > **Uzantılar ve güncelleştirmeler**. İçinde **Uzantılar ve güncelleştirmeler** iletişim kutusunda, **yüklü** solda, kategori ve uzantısı adına göre arayın.

::: moniker-end

::: moniker range=">=vs-2019"

Seçeneğini yüklü olup olmadığını ' uzantısı denetlemek istiyorsanız **uzantıları** > **uzantıları yönetme**. İçinde **uzantıları yönetme** iletişim kutusunda **yüklü** solda, kategori ve sonra uzantıyı adıyla Ara.

::: moniker-end

## <a name="next-steps"></a>Sonraki adımlar

> [!div class="nextstepaction"]
> [Roslyn çözümleyicilerini Visual Studio'da kullanın](../code-quality/use-roslyn-analyzers.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Roslyn çözümleyicilerini Visual Studio'da genel bakış](../code-quality/roslyn-analyzers-overview.md)
- [FxCop Çözümleyicileri yükleyin](../code-quality/install-fxcop-analyzers.md)