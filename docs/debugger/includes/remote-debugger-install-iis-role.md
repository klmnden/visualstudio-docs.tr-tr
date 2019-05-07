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
ms.openlocfilehash: 13ca035b01ec8af1277d70b3c792293a1af4687a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62908050"
---
Bu adımlar, IIS'nin yalnızca bir temel yapılandırmasını gösterir. Daha ayrıntılı bilgi için veya bir Windows Masaüstü makineye yüklemek için bkz: [IIS yayımlama](/aspnet/core/publishing/iis?tabs=aspnetcore2x#iis-configuration) veya [IIS 8.0 kullanarak ASP.NET 3.5 ve ASP.NET 4.5](/iis/get-started/whats-new-in-iis-8/iis-80-using-aspnet-35-and-aspnet-45).

Windows Server işletim sistemleri için **rol ve Özellik Ekle** Sihirbazı aracılığıyla **Yönet** bağlantı veya **Pano** bağlantısını **Sunucu Yöneticisi'ni**. Üzerinde **sunucu rolleri** kutusunu işaretleyin, adım **Web sunucusu (IIS)**.

![Web sunucusu IIS rolünü sunucu rolleri adımda seçilir.](../media/remotedbg-server-roles-ws2012.png)

Üzerinde **rol hizmetlerini** adım, istediğiniz veya varsayılan rol hizmetlerini sağlanan kabul IIS rol hizmetlerini seçin. Dağıtım kullanarak etkinleştirmek istiyorsanız emin olun, ayarları ve Web dağıtımı yayımlama **IIS Yönetim betikleri ve araçları** seçilir.

Hizmetleri ve web sunucusu rolü yüklemek için onay adımlara devam edin. Web sunucusu (IIS) rolünü yükledikten sonra özelliği sunucusu/IIS yeniden başlatma gerekli değildir.