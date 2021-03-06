---
title: Visual C++ projesinde uzaktan hata ayıklama | Microsoft Docs
ms.custom: remotedebugging
ms.date: 08/14/2018
ms.topic: conceptual
dev_langs:
- C++
- FSharp
- CSharp
- JScript
- VB
helpviewer_keywords:
- remote debugging, setup
ms.assetid: 8b8eca0d-122f-4eda-848a-cf0945f207d0
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: 81a5ebba2d14a0e091b3b0bcd78a066ef50ed759
ms.sourcegitcommit: ea182703e922c74725045afc251bcebac305068a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71211117"
---
# <a name="remote-debugging-a-visual-c-project-in-visual-studio"></a>Visual Studio 'da bir C++ Visual projesinde uzaktan hata ayıklama
Farklı bir bilgisayardaki Visual Studio uygulamasında hata ayıklamak için, uygulamanızı dağıtacağınız bilgisayara Uzak araçları yükleyip çalıştırın, projenizi Visual Studio 'dan uzak bilgisayara bağlanacak şekilde yapılandırın ve ardından uygulamanızı dağıtıp çalıştırın.

![Uzaktan hata ayıklayıcı bileşenleri](../debugger/media/remote-debugger-client-apps.png "Remote_debugger_components")

Uzaktan hata ayıklama Evrensel Windows uygulamaları (UWP) hakkında daha fazla bilgi için bkz. [bir yüklenen uygulama paketinin hatalarını ayıklama](debug-installed-app-package.md).

## <a name="requirements"></a>Gereksinimler

Desteklenen Windows 7 ve daha yeni uzaktan hata ayıklayıcı (telefon değil) ve Windows Server 2008 Service Pack 2'ile başlayan Windows Server sürümleri. Gereksinimlerinin tam listesi için bkz. [gereksinimleri](../debugger/remote-debugging.md#requirements_msvsmon).

> [!NOTE]
> Bir proxy üzerinden bağlı iki bilgisayar arasında hata ayıklama desteklenmiyor. Ülkeler yüksek gecikme süresi veya çevirmeli, Internet gibi düşük bant genişliği bağlantı üzerinden veya Internet üzerinden hata ayıklama önerilmez ve başarısız olabilir veya edilemeyecek kadar yavaş.

## <a name="download-and-install-the-remote-tools"></a>Uzak araçları indirme ve yükleme

[!INCLUDE [remote-debugger-download](../debugger/includes/remote-debugger-download.md)]

> [!TIP]
> Bazı senaryolarda, uzaktan hata ayıklayıcıyı bir dosya paylaşımından çalıştırma en verimli olabilir. Daha fazla bilgi için [uzaktan hata ayıklayıcıyı bir dosya paylaşımından çalıştırma](../debugger/remote-debugging.md#fileshare_msvsmon).

## <a name="BKMK_setup"></a> Uzaktan hata ayıklayıcı ayarlayın

[!INCLUDE [remote-debugger-configuration](../debugger/includes/remote-debugger-configuration.md)]

> [!NOTE]
> Gerektiğinde ek kullanıcılar için izinler eklemek için kimlik doğrulama modunu değiştirmek veya bağlantı noktası numarası için uzaktan hata ayıklayıcı değilse [uzaktan hata ayıklayıcı yapılandırma](../debugger/remote-debugging.md#configure_msvsmon).

## <a name="remote_cplusplus"></a>Visual C++ projesinde uzaktan hata ayıklama
 Aşağıdaki yordamda, projenin adı ve yolu C:\remotetemp\MyMfc olur ve uzak bilgisayarın adı **Mjo-DL**' dir.

1. **Mymfc** ADLı bir MFC uygulaması oluşturun.

2. Uygulamasının başlangıcında, **MainFrm. cpp**gibi `CMainFrame::OnCreate`kolayca ulaşılan uygulamada herhangi bir yere bir kesme noktası ayarlayın.

3. Çözüm Gezgini, projeye sağ tıklayın ve **Özellikler**' i seçin. **Hata ayıklama** sekmesini açın.

4. Hata ayıklayıcıyı **uzak Windows hata ayıklayıcıya** **başlatılacak şekilde** ayarlayın.

    ![RemoteDebuggingCPlus](../debugger/media/remotedebuggingcplus.png "RemoteDebuggingCPlus")

5. Özelliklerde aşağıdaki değişiklikleri yapın:

   |Ayar|Değer|
   |-|-|
   |Uzak komut|C:\remotetemp\mymfc.exe|
   |Çalışma dizini|C:\remotetemp|
   |Uzak sunucu adı|MJO-DL:*BağlantıNoktasıNumarası*|
   |Bağlantı|Windows kimlik doğrulaması ile uzaktan|
   |Hata ayıklayıcı türü|Yalnızca yerel|
   |Dağıtım dizini|Ni c:\remotetemp|
   |Dağıtılacak ek dosyalar|C:\data\mymfcdata.exe.|

    Ek dosyalar dağıtırsanız (isteğe bağlı), klasörün her iki makinede de mevcut olması gerekir.

6. Çözüm Gezgini, çözüme sağ tıklayın ve **Configuration Manager**' i seçin.

7. **Hata ayıklama** yapılandırması için **Dağıt** onay kutusunu seçin.

    ![Remotedebugcplusdeploy](../debugger/media/remotedebugcplusdeploy.png "Remotedebugcplusdeploy")

8. Hata ayıklamayı Başlat (hata ayıklama **> başlatın**veya **F5**).

9. Yürütülebilir dosya otomatik olarak uzak bilgisayara dağıtılır.

10. İstenirse, uzak makineye bağlanmak için ağ kimlik bilgilerini girin.

     Gerekli kimlik bilgileri ağınızın güvenlik yapılandırmasına özgüdür. Örneğin, bir etki alanı bilgisayarında bir güvenlik sertifikası seçebilir veya etki alanı adınızı ve parolanızı girebilirsiniz. Bir etki alanı olmayan makinede, makine adı ve geçerli kullanıcı hesabı adı gibi girebilirsiniz <strong>MJO-DL\name@something.com</strong>, doğru parola ile birlikte.

11. Visual Studio bilgisayarında yürütmenin kesme noktasında durdurulduğunu görmeniz gerekir.

    > [!TIP]
    > Alternatif olarak, dosyaları ayrı bir adım olarak dağıtabilirsiniz. **Çözüm Gezgini,** **mymfc** düğümüne sağ tıklayın ve ardından **Dağıt**' ı seçin.

    Uygulama için gerekli kod olmayan dosyalarınız varsa, bu dosyaları **uzak Windows hata ayıklayıcı** sayfasında **dağıtılacak ek dosyalar** içinde belirtebilirsiniz.

    Alternatif olarak, dosyaları projenize dahil edebilir ve her bir dosyanın **Özellikler** sayfasında **içerik** özelliğini **Evet** olarak ayarlayabilirsiniz. Bu dosyalar, **uzak Windows hata ayıklayıcı** sayfasında belirtilen **dağıtım dizinine** kopyalanır. Ayrıca, **dosya kopyalamak** Için **öğe türünü** değiştirebilir ve dosyaların **dağıtım dizininin**bir alt klasörüne kopyalanması gerekiyorsa ek özellikler belirtebilirsiniz.

## <a name="set-up-debugging-with-remote-symbols"></a>Uzak simgeleri ile hata ayıklamayı kurma

[!INCLUDE [remote-debugger-symbols](../debugger/includes/remote-debugger-symbols.md)]

## <a name="see-also"></a>Ayrıca Bkz.
- [Visual Studio’da hata ayıklama](../debugger/index.yml)
- [Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)
- [Windows Güvenlik Duvarı’nı Uzaktan Hata Ayıklama İçin Yapılandırma](../debugger/configure-the-windows-firewall-for-remote-debugging.md)
- [Uzaktan Hata Ayıklayıcı Bağlantı Noktası Atamaları](../debugger/remote-debugger-port-assignments.md)
- [Uzak IIS Bilgisayarında Uzaktan ASP.NET ile Hata Ayıklama](../debugger/remote-debugging-aspnet-on-a-remote-iis-computer.md)
- [Uzaktan Hata Ayıklama Hataları ve Sorun Giderme](../debugger/remote-debugging-errors-and-troubleshooting.md)