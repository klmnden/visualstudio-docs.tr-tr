---
title: VSIX paketlerini imzalama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- signature
- signing
- authenticode
- vsix
- packages
ms.assetid: e34cfc2c-361c-44f8-9cfe-9f2be229d248
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 710cc523cdd01ad431572860ace9b06af3cff418
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66332088"
---
# <a name="signing-vsix-packages"></a>VSIX Paketlerini İmzalama
Uzantı derlemelerini Visual Studio'da çalışabilirler, ancak bunu yapmak için iyi bir uygulamadır önce oturum açmanız gerekmez.

 Uzantınızı güvenli ve ile değiştirilmediğinden emin olmak istiyorsanız, VSIX paketine bir dijital imza ekleyebilirsiniz. Bir VSIX imzalandığında VSIX yükleyici, imza hakkında daha fazla bilgi artı imzalanmış olduğunu belirten bir ileti görüntülenir. VSIX içeriğini değiştirilmiş ve VSIX yeniden imzalı değil, VSIX yükleyici imzası geçerli değil gösterilir. Yükleme durdurulmadı, ancak kullanıcı uyarılır.

> [!IMPORTANT]
> Visual Studio 2015 ile başlayarak, VSIX paketlerini SHA256 şifreleme dışında herhangi bir şey ile imzalanmış geçersiz imzaya sahip olunması olarak tanımlanır. VSIX yüklemesi engellenmez, ancak kullanıcı uyarılır.

## <a name="signing-a-vsix-with-vsixsigntool"></a>Bir VSIX VSIXSignTool ile imzalama
 İmzalama aracı bulunan bir SHA256 şifreleme yok [VisualStudioExtensibility](http://www.nuget.org/profiles/VisualStudioExtensibility) nuget.org [VsixSignTool](http://www.nuget.org/packages/Microsoft.VSSDK.Vsixsigntool).

#### <a name="to-use-the-vsixsigntool"></a>VSIXSignTool kullanmak için

1. Kendi VSIX bir projeye ekleyin.

2. Çözüm Gezgini'nde proje düğümüne sağ tıklayın seçerek **Ekle &#124; NuGet paketlerini Yönet**.  NuGet ve NuGet ekleme hakkında daha fazla bilgi için bkz: paketleri [NuGet belgeleri](/NuGet) ve [Paket Yöneticisi UI](/NuGet/Tools/Package-Manager-UI) konuları.

3. VSIXSignTool VisualStudioExtensibility gelen arayın ve NuGet paketini yükleyin.

4. Şimdi, VSIXSignTool projenin yerel paketleri konumundan çalıştırabilirsiniz. İmzalama senaryonuz için Aracı'nın komut satırı yardımına bakın (VSIXSignTool.exe /?).

   Örneğin: bir parola korumalı bir sertifika dosyası ile imzala

   VSIXSignTool.exe oturum /f \<certfile > /p \<parola > \<VSIXfile >

## <a name="see-also"></a>Ayrıca Bkz.
- [Visual Studio Uzantıları Gönderme](../extensibility/shipping-visual-studio-extensions.md)
