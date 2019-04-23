---
title: 'Hata: DCOM iletişimi başlatılamıyor | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.unmarshal_server_failed
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
ms.openlocfilehash: 1112ec72e8aca764f749a6d8f1925302f569b17e
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60044790"
---
# <a name="error-unable-to-initiate-dcom-communication"></a>Hata: DCOM iletişimi başlatılamıyor
Yerel makinede Uzak makineyle iletişim kurmak çalışırken bir DCOM hatası oluştu. Bu bir güvenlik duvarı uzak sunucuda veya uzak makinede bozuk Windows kimlik doğrulaması kaynaklanır.

### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

- Uzak makinede Windows Güvenlik duvarı varsa, bkz. [uzaktan hata ayıklama](../debugger/remote-debugging.md) yerel hata ayıklama için güvenlik duvarını yapılandırma hakkında yönergeler için.

- Windows kimlik doğrulama geri yüklemek için her iki makine yeniden deneyin. Yerel ve Uzak makinelerde Kerberos hataları için olay günlüklerini inceleyin ve bilinen sorunlar için etki alanı yöneticileri ile iletişime geçin.

## <a name="see-also"></a>Ayrıca Bkz.
- [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)