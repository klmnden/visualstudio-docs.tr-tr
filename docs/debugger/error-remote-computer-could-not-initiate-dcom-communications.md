---
title: 'Hata: Uzak bilgisayar DCOM iletişimini başlatamıyor | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.unmarshal_callback_failed
dev_langs:
- CSharp
- VB
- FSharp
- C++
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9e936292010c73decffadc5b215156f2200ed8b3
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56683080"
---
# <a name="error-remote-computer-could-not-initiate-dcom-communications"></a>Hata: Uzak bilgisayar DCOM iletişimini başlatamadı
Uzak makinede yerel makine ile iletişim kurmak çalışırken bir DCOM hatası oluştu. Yerel makine olduğu makinedir

 Visual Studio çalışıyor. Bu hata, çeşitli nedenlerle oluşabilir:

-   Yerel makine etkin bir güvenlik duvarı vardır.

-   Yerel makinede uzak makineden Windows kimlik doğrulaması çalışmıyor.

### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

1.  Yerel makinede Windows Güvenlik duvarı varsa, bkz. [uzaktan hata ayıklama](../debugger/remote-debugging.md) yerel hata ayıklama için güvenlik duvarını yapılandırma hakkında yönergeler için.

2.  Uzak sunucudan yerel makine üzerindeki bir dosya paylaşımına açmaya çalışırken tarafından Windows kimlik doğrulamasını Sına.

3.  Windows kimlik doğrulama geri yüklemek için her iki makine yeniden deneyin. Yerel ve Uzak makinelerde Kerberos hataları için olay günlüklerini inceleyin ve bilinen sorunlar için etki alanı yöneticileri ile iletişime geçin.

## <a name="see-also"></a>Ayrıca Bkz.
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)