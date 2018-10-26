---
title: Uzaktan hata ayıklama için Windows Güvenlik Duvarı yapılandırma | Microsoft Docs
ms.custom: ''
ms.date: 05/18/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 66e3230a-d195-4473-bbce-8ca198516014
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 7f6904313ff585b8099c993f83e90bacb91a4ba2
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49847961"
---
# <a name="configure-the-windows-firewall-for-remote-debugging"></a>Uzaktan hata ayıklama için Windows Güvenlik duvarını yapılandırma
Bu konu, aşağıdaki işletim sistemlerini çalıştıran bilgisayarlarda uzaktan hata ayıklamayı etkinleştirmek için Güvenlik Duvarı'nı yapılandırmak açıklar:  
  
- Windows 10  
  
- Windows 8/8.1  
  
- Windows 7   
  
- Windows Server 2012 R2  

- Windows Server 2012
  
- Windows Server 2008 R2 
  
  Bu yapılandırma üzerinde hata ayıklaması yapıyorsanız ağ güvenlik duvarı tarafından korumalı değilse gereksizdir. Aksi takdirde, hem Visual Studio barındıran bilgisayarda hem de ayıklanacak uzak bilgisayarda güvenlik duvarı yapılandırması değişiklikleri gerektirir.  
  
  **IPSec** ağınız iletişimin gerektiriyorsa olması IPSec kullanarak gerçekleştirilen, hem Visual Studio ana bilgisayar hem de uzak bilgisayara ek bağlantı noktalarını açmanız gerekir.  
  
  **Web sunucusu** uzak bir Web sunucusunda hata ayıklaması yapıyorsanız, uzak bilgisayardaki ek bir bağlantı noktası açmanız gerekir. (IIS için bağlantı noktası 80 açık olması gerekir.)  
  
  Her iki bilgisayar aynı işletim sistemini çalıştırmak olmadığını unutmayın. Örneğin, Visual Studio bilgisayarı, Windows 10 çalıştırabilirsiniz ve Windows Server 2012 R2 Uzak bilgisayarda çalıştırabilirsiniz.      
  
## <a name="ports-on-the-remote-computer-that-enable-remote-debugging"></a>Uzak bilgisayarda uzaktan hata ayıklamayı etkinleştirme bağlantı  
  
|**Bağlantı Noktaları**|**Gelen ve giden**|**Protokolü**|**Açıklama**|   
|-|-|-|-|  
|4022|gelen|TCP|VS 2017 için. Her bir Visual Studio sürümü için 2 bağlantı noktası numarası artırılır. Daha fazla bilgi için [Visual Studio uzaktan hata ayıklayıcı bağlantı noktası atamaları](../debugger/remote-debugger-port-assignments.md).|  
|4023|gelen|TCP|VS 2017 için. Her bir Visual Studio sürümü için 2 bağlantı noktası numarası artırılır. (Yalnızca kullanılan uzaktan hata ayıklama uzaktan hata ayıklayıcı 64-bit sürümünden 32 bitlik bir işlem.) Daha fazla bilgi için [Visual Studio uzaktan hata ayıklayıcı bağlantı noktası atamaları](../debugger/remote-debugger-port-assignments.md).| 
|3702|Giden|UDP|(İsteğe bağlı) Uzaktan hata ayıklayıcı bulma işlemi için gereklidir.|    
  
## <a name="how-to-configure-ports-in-windows-firewall"></a>Windows Güvenlik Duvarı bağlantı noktalarını yapılandırma  

Visual Studio veya uzaktan hata ayıklayıcı yüklediğinizde, yazılım doğru bağlantı noktalarını açmayı deneyecek. Ancak, (örneğin, bir üçüncü taraf Güvenlik Duvarı'nı kullanarak) Bazı senaryolarda, el ile bir bağlantı noktası açmanız gerekebilir. Bağlantı noktalarının açık olduğunu doğrulamak gerekiyorsa bkz [sorun giderme](#troubleshooting). Bir bağlantı noktası açmak için bazı yönergeler eski Windows sürümleri üzerinde farklı olabilir.

Bir bağlantı noktasını açmak için:
  
1. Açık **Başlat** menüsünde **Gelişmiş Güvenlik Özellikli Windows Güvenlik Duvarı**.

2. Ardından **gelen kuralları > Yeni Kural > bağlantı noktası**ve ardından **sonraki**. (Giden kuralları için seçin **giden kuralları** yerine.)

3. Seçin ya da **TCP** veya **UDP**bağlı olarak bağlantı noktası numarası.

4. Altında **belirli yerel bağlantı noktaları**, bağlantı noktası numarasını girin, tıklayın **sonraki**.

5. Tıklayın **bağlantıya izin** ve ardından **sonraki**.

6. İçin bağlantı noktasını etkinleştirmek ve bir veya daha fazla ağ türlerini seçmek **sonraki**.

    Seçtiğiniz türü, uzak bilgisayarın bağlı olduğu ağ içermelidir.
7. Ad ekleyin (örneğin, **msvsmon**, **IIS**, veya **Web dağıtımı**) tıklayın ve kural için **son**.

    Yeni kuralınıza kuralları gelen veya giden kuralları listesinde görmeniz gerekir.

## <a name="troubleshooting"></a>Sorun giderme

Uzaktan hata ayıklayıcı ile uygulamanıza ekleme ile ilgili sorunlar yaşıyorsanız, doğru bağlantı noktalarının açık olduğunu doğrulamak gerekebilir.

### <a name="verify-that-ports-are-open-in-the-windows-firewall-on-the-visual-studio-computer"></a>Bağlantı noktaları Visual Studio bilgisayardaki Windows Güvenlik Duvarı'nda açık olduğundan emin olun  
 Windows Güvenlik Duvarı yapılandırma yönergeleri biraz daha farklı işletim sistemleri üzerinde farklı. Windows 8/8.1, Windows 10 ve Windows Server 2012, word **uygulama** kullanılır; Windows 7 veya Windows Server 2008, word **program** kullanılır.  Aşağıdaki adımlarda word kullanacağız **uygulama**.  
  
1.  Windows Güvenlik Duvarı sayfasını açın. (İçinde **Başlat** menü arama kutusuna **Windows Güvenlik Duvarı**).  
  
2.  Tıklayın **bir uygulama veya özelliğin Windows Güvenlik Duvarı üzerinden izin**.  
  
3.  İçinde **izin verilen uygulamalar ve Özellikler** listesinde, Aranan **Visual Studio uzaktan hata ayıklayıcı bulma**. Listeleniyorsa, seçili olduğunu ve bir veya daha fazla ağ türü ayrıca seçildiğinden emin olun.  
  
4.  Varsa **Visual Studio uzaktan hata ayıklayıcı bulma** olan listelenmeyen tıklayın **başka bir uygulamanın ver**. İçinde hala görmüyorsanız, **uygulama ekleme** penceresinde tıklayın **Gözat** gidin  **\<Visual Studio yükleme dizini > \Common7\IDE\Remotehataayıklayıcı**. (X86, x64, Appx) uygulama için ilgili klasörü bulun ve ardından **msvsmon.exe**. Ardından **Ekle**.  
  
5.  İçinde **izin verilen uygulamalar ve Özellikler** listesinden **Visual Studio uzaktan hata ayıklayıcı**. Bir veya daha fazla ağ türlerini denetleyin (**etki alanı, ev/iş (özel), ortak**) ile iletişim kurmak için uzaktan hata ayıklama İzleyicisi istiyor. Visual Studio bilgisayarın bağlı olduğu ağ türleri eklemeniz gerekir. 

### <a name="verify-that-ports-are-open-in-the-windows-firewall-on-the-remote-computer"></a>Bağlantı noktalarını uzak bilgisayarda Windows Güvenlik Duvarı'nda açık olduğundan emin olun  
 Uzaktan hata ayıklama bileşenlerini, uzak bilgisayarda yüklü veya paylaşılan bir dizinden çalıştırabilirsiniz. Güvenlik duvarının uzak bilgisayar, her iki durumda da yapılandırılması gerekir. Uzaktan hata ayıklama bileşenleri bulunur:  
  
 **\<Visual Studio yükleme dizini > \Common7\IDE\Remote hata ayıklayıcı**  
  
 Windows Güvenlik Duvarı yapılandırma yönergeleri biraz daha farklı işletim sistemleri üzerinde farklı. Windows 8/8.1, Windows 10 ve Windows Server 2012, word **uygulama** kullanılır; Windows 7 veya Windows Server 2008, word **program** kullanılır.  Aşağıdaki adımlarda word kullanacağız **uygulama**.  
  
1.  Windows Güvenlik Duvarı sayfasını açın. (Üzerinde **Başlat** menü arama kutusuna **Windows Güvenlik Duvarı**.)  
  
2.  Tıklayın **bir uygulama veya özelliğin Windows Güvenlik Duvarı üzerinden izin**.  
  
3.  İçinde **izin verilen uygulamalar ve Özellikler** listesinde, Aranan **Visual Studio uzaktan hata ayıklayıcı**. Listeleniyorsa, seçili olduğunu ve bir veya daha fazla ağ türü ayrıca seçildiğinden emin olun.  
  
4.  Varsa **Visual Studio uzaktan hata ayıklayıcı** olan listelenmeyen tıklayın **başka bir uygulamanın ver**. İçinde hala görmüyorsanız, **ekleme uygulama penceresi**, tıklayın **Gözat** gidin  **\<Visual Studio yükleme dizini > \Common7\IDE\Remotehataayıklayıcı**. (X86, x64, Appx) uygulama için ilgili klasörü bulun ve ardından **msvsmon.exe**. Ardından **Ekle**.  
  
5.  İçinde **izin verilen uygulamalar** listesinden **Visual Studio uzaktan hata ayıklayıcı**. Bir veya daha fazla ağ türlerini denetleyin (**etki alanı, ev/iş (özel), ortak**) ile iletişim kurmak için uzaktan hata ayıklama İzleyicisi istiyor. Visual Studio bilgisayarın bağlı olduğu ağ türleri eklemeniz gerekir. 

### <a name="managed-or-native-compatibility-mode-open-additional-ports-on-the-remote-computer"></a>(Yönetilen veya yerel uyumluluk modu) Uzak bilgisayarda ek bağlantı noktalarını açma

Hata ayıklayıcı için Uyumluluk modu kullanıyorsanız (**Araçlar > Seçenekler > hata ayıklama**), ek bağlantı noktalarını açılması gerekir. Hata ayıklayıcının eski bir sürümü Uyumluluk modunu etkinleştirir ve farklı bağlantı noktaları gereklidir.

> [!NOTE]
> Hata ayıklayıcının eski bir sürümü Visual Studio 2010 Hata Ayıklayıcı ' dir.
  
|**Bağlantı Noktaları**|**Gelen ve giden**|**Protokolü**|**Açıklama**|  
|-|-|-|-|  
|135, 139, 445|Giden|TCP|Gerekli.|  
|137, 138|Giden|UDP|Gerekli.|  
|500, 4500|Giden|UDP|Etki alanı ilkeniz ağ iletişimi, IPSec gerçekleştirilmesini gerektiriyorsa gereklidir.|  
|80|Giden|TCP|Web sunucusu hata ayıklama için gereklidir.|
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)