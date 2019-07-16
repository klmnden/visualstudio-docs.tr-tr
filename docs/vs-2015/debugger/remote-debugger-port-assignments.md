---
title: Uzaktan hata ayıklayıcı bağlantı noktası atamaları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 238bb4ec-bb00-4c2b-986e-18ac278f3959
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: c1e70ec3ba50e5be1ed532bb4a88cbdd500af09c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68195168"
---
# <a name="remote-debugger-port-assignments"></a>Uzaktan Hata Ayıklayıcı Bağlantı Noktası Atamaları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio uzaktan hata ayıklayıcı, bir uygulama veya bir arka plan hizmeti olarak çalıştırabilirsiniz. Bir uygulama olarak yürütüldüğünde, varsayılan olarak şu şekilde atanan bir bağlantı noktası kullanır:  
  
- Visual Studio 2015: 4020  
  
- Visual Studio 2013 için: 4018  
  
- Visual Studio 2012 için: 4016  
  
  Diğer bir deyişle, her sürüm için 2 tarafından uzaktan hata ayıklayıcı için atanan bağlantı noktası numarası artırılır. Farklı bir bağlantı noktası numarası gibi ayarlayabilirsiniz. Şu bağlantı noktası numaraları daha sonraki bir bölümde ayarlama açıklanmaktadır.  
  
## <a name="the-remote-debugger-port-on-32-bit-operating-systems"></a>32 bit işletim sistemlerinde uzaktan hata ayıklayıcı bağlantı noktası  
 (Visual Studio 2015) gelen TCP 4020 ana bağlantı noktası ve tüm senaryolar için gereklidir. Bu komut satırı veya uzaktan hata ayıklayıcı penceresinde yapılandırabilirsiniz.  
  
 Uzaktan hata ayıklayıcı penceresinde **Araçlar / Seçenekler**, TCP/IP bağlantı noktası numarasını ayarlayın.  
  
 Uzaktan hata ayıklayıcı ile komut satırında başlatmak **/bağlantı noktası** geçiş: **msvsmon/Port \<bağlantı noktası numarası >** .  
  
 Komut satırı anahtarları hata ayıklama Uzaktan Yardım'daki tüm uzaktan hata ayıklayıcıyı bulabilirsiniz (basın **F1** veya **Yardım / kullanım** uzaktan hata ayıklayıcı penceresinde).  
  
## <a name="the-remote-debugger-port-on-64-bit-operating-systems"></a>64-bit işletim sistemlerinde uzaktan hata ayıklayıcı bağlantı noktası  
 Uzaktan hata ayıklayıcı 64-bit sürümünü başlatıldığında, varsayılan olarak 4020 bağlantı noktasını kullanır.  Bir 32 bit işlemde hata ayıklamak, uzaktan hata ayıklayıcı 64-bit sürümünü 4021 bağlantı noktası üzerinde uzaktan hata ayıklayıcı bir 32-bit sürümü başlatır. 32-bit uzaktan hata ayıklayıcı çalıştırırsanız, 4020 kullanır ve 4021 kullanılmaz.  
  
 Bu bağlantı noktası, komut satırından yapılandırılabilir: **Msvsmon/wow64port \<bağlantı noktası numarası >** .  
  
## <a name="the-discovery-port"></a>Bulma bağlantı noktası  
 UDP 3702, ağ üzerinde çalışan uzaktan hata ayıklayıcı örneklerini bulmak için kullanılır (örneğin, **Bul** iletişim kutusunda **iliştirme** iletişim). Yalnızca makine adı veya IP adresi hedef bilgisayarın olduğunu bilmesinin başka bir şekilde varsa isteğe bağlı, bu nedenle uzaktan hata ayıklayıcı, çalışan bir makine bulmak için kullanılır. Bağlantı noktası numarası yapılandırılamaz için bu bulma, standart bir bağlantı noktasıdır.  
  
 Bulmayı etkinleştirmek istemiyorsanız, devre dışı keşif ile komut satırından msvsmon başlatabilirsiniz:  **Msvsmon /nodiscovery**.  
  
## <a name="remote-debugger-ports-on-azure"></a>Azure uzaktan hata ayıklayıcı bağlantı noktaları  
 Aşağıdaki bağlantı noktaları, Azure üzerinde uzaktan hata ayıklayıcı tarafından kullanılır. Bulut hizmeti bağlantı noktalarını tek tek bir VM üzerindeki bağlantı noktalarına eşlenir. TCP tüm bağlantı noktaları şunlardır.  
  
||||  
|-|-|-|  
|**bağlantı**|**Bulut hizmeti bağlantı noktası**|**VM üzerindeki bağlantı noktası**|  
|Microsoft.WindowsAzure.Plugins.RemoteDebugger.Connector|30400|30398|  
|Microsoft.WindowsAzure.Plugins.RemoteDebugger.Forwarder|31400|31398|  
|Microsoft.WindowsAzure.Plugins.RemoteDebugger.FileUpload|32400|32398|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)
