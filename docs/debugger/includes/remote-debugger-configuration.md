---
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.openlocfilehash: 2e5782c49f26925d9eda81f04653b1a20666c6b1
ms.sourcegitcommit: 748d9cd7328a30f8c80ce42198a94a4b5e869f26
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/15/2019
ms.locfileid: "68149164"
---
1. Uzak bilgisayarda bulmak ve başlatmak **uzaktan hata ayıklayıcı** gelen **Başlat** menüsü. 
   
   Uzak bilgisayarda yönetici izinlerine sahip değilseniz, sağ **uzaktan hata ayıklayıcı** seçin **yönetici olarak çalıştır**. Aksi takdirde, yalnızca başlatın normalde.

   Ekleme planlıyorsanız bir yönetici olarak çalıştırdığınızdan veya farklı bir kullanıcı altında çalışan bir işlemi (IIS gibi) hesabı, sağ **uzaktan hata ayıklayıcı** seçin **yöneticiolarakçalıştır**. Daha fazla bilgi için [uzaktan hata ayıklayıcı yönetici olarak çalıştır](../remote-debugging-errors-and-troubleshooting.md#run-the-remote-debugger-as-an-administrator).
   
1. İlk kez uzaktan hata ayıklayıcıyı başlattığınızda (veya önce yapılandırdığınızdan,), **uzaktan hata ayıklama Yapılandırması** iletişim kutusu görüntülenir.  
  
    ![Uzaktan hata ayıklayıcı yapılandırma](../media/remotedebuggerconfwizardpage.png "uzaktan hata ayıklayıcı yapılandırma")  
  
1. Windows Web Servisleri API, yalnızca Windows Server 2008 R2 üzerinde gerçekleşen yüklü değilse, seçin **yükleme** düğmesi.  
  
1. Uzak Araçlar üzerinde kullanmak istediğiniz en az bir ağ türünü seçin. Bilgisayarları bir etki alanına bağlıysanız, ilk öğe seçmeniz gerekir. Bilgisayar bir çalışma grubunda veya ev grubu bağlıysa, uygun şekilde ikinci veya üçüncü öğeyi seçin.  
  
1. Seçin **uzaktan hata ayıklamayı Yapılandır** güvenlik duvarını yapılandırmak ve uzaktan hata ayıklayıcıyı başlatın.  
  
1. Yapılandırma tamamlandığında, **uzaktan hata ayıklayıcı** penceresi görüntülenir.
  
    ![Uzaktan hata ayıklayıcı penceresini](../media/remotedebuggerwindow.png "uzaktan hata ayıklayıcı penceresi")
  
    Uzaktan hata ayıklayıcı şimdi bir bağlantı için bekliyor. Sunucu adı ve bağlantı noktası numarasına uzaktan bağlantı yapılandırmasını Visual Studio'da ayarlayın.  
  
Uzaktan hata ayıklayıcıyı durdurmak için seçin **dosya** > **çıkış**. Buradan yeniden **Başlat** menüsünden veya komut satırından:  
  
```cmd
<Remote debugger installation directory>\msvsmon.exe
```
