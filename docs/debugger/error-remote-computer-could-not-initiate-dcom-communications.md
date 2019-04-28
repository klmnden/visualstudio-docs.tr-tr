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
ms.openlocfilehash: 7ceb796b3a4b3cbc2b239a09ac8c173e746f194c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62850902"
---
# <a name="error-remote-computer-could-not-initiate-dcom-communications"></a>Hata: Uzak bilgisayar DCOM iletişimini başlatamadı
Uzak makinede yerel makine ile iletişim kurmak çalışırken bir DCOM hatası oluştu. Yerel makine olduğu makinedir

 Visual Studio çalışıyor. Bu hata, çeşitli nedenlerle oluşabilir:

- Yerel makine etkin bir güvenlik duvarı vardır.

- Yerel makinede uzak makineden Windows kimlik doğrulaması çalışmıyor.

### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

1. Yerel makinede Windows Güvenlik duvarı varsa, bkz. [uzaktan hata ayıklama](../debugger/remote-debugging.md) yerel hata ayıklama için güvenlik duvarını yapılandırma hakkında yönergeler için.

2. Uzak sunucudan yerel makine üzerindeki bir dosya paylaşımına açmaya çalışırken tarafından Windows kimlik doğrulamasını Sına.

3. Windows kimlik doğrulama geri yüklemek için her iki makine yeniden deneyin. Yerel ve Uzak makinelerde Kerberos hataları için olay günlüklerini inceleyin ve bilinen sorunlar için etki alanı yöneticileri ile iletişime geçin.

## <a name="see-also"></a>Ayrıca Bkz.
 [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)