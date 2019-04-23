---
title: 'Nasıl yapılır: ClickOnce uygulamasına Önkoşullar dahil etme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: c66bf0a5-8c93-4e68-a224-3b29ac36fe4d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 57d89fec51cf73d310e3ad2e18b3d4270bd8ff74
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60041987"
---
# <a name="how-to-include-prerequisites-with-a-clickonce-application"></a>Nasıl yapılır: ClickOnce uygulamasına Önkoşullar dahil etme
Önkoşul yazılımı dağıtmadan önce bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulaması gerekir indirmeniz olan yükleme paketlerini geliştirme bilgisayarınıza bu Önkoşullar. Ne zaman bir uygulamayı yayımlamak ve seçin **Uygulamamla aynı konumdan önkoşulları karşıdan**, eğer yükleyici paketleri olmayan bir hata meydana gelir **paketleri** klasör.

> [!NOTE]
>  .NET Framework için bir yükleyici paket eklemek için bkz [geliştiriciler için .NET Framework Dağıtım Kılavuzu](/dotnet/framework/deployment/deployment-guide-for-developers).

## <a name="Package"></a> Package.xml kullanarak bir yükleyici paket eklemek için

1. Dosya Gezgini'nde Aç **paketleri** klasör.

    Varsayılan olarak, yoludur `%ProgramFiles(x86)%\Microsoft SDKs\ClickOnce Bootstrapper\Packages\`.

2. Eklemek istediğiniz ön koşul için klasörü açın ve ardından'ın yüklü sürümü için dil klasörü açın [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] (örneğin, **tr** İngilizce).

3. Not Defteri'nde açın *Package.xml* dosya.

4. Bulun **adı** öğesini içeren **http://go.microsoft.com/fwlink**ve URL'yi kopyalayın. Dahil **LinkId** bölümü.

   > [!NOTE]
   >  Hayır ise **adı** ögesinin **http://go.microsoft.com/fwlink**açın **Product.xml** bulun ve ön koşul için kök klasöründeki dosya **fwlink** dize.

   > [!IMPORTANT]
   >  Bazı ön koşullar (örneğin, 32-bit veya 64-bit sistemler için) birden çok yükleme paketine sahiptirler. Birden çok **adı** öğeleri içeren **fwlink**, bunların her biri için kalan adımları yinelemeniz gerekir.

5. Tarayıcınızın adres çubuğuna URL'yi yapıştırın ve ardından, çalıştırmanız veya kaydetmeniz istendiğinde **Kaydet**.

    Bu adım, yükleyici dosyasını bilgisayarınıza yükler.

6. Dosyayı ön koşul için kök klasörüne kopyalayın.

    Örneğin, Windows Installer 4.5 ön için dosyaya kopyalayın *\Packages\WindowsInstaller4_5* klasör.

    Şimdi, yükleyici paketi uygulamanız ile dağıtabilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: ClickOnce uygulamasıyla önkoşulları işaretli yükleyin](../deployment/how-to-install-prerequisites-with-a-clickonce-application.md)
