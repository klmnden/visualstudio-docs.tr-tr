---
title: 'Hata: Web sunucusu istenen kaynağı bulamadı. | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugger, Web application errors
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c0b37e96db46a43b869867b8b5e37f857e75aff9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62850274"
---
# <a name="error-the-web-server-could-not-find-the-requested-resource"></a>Hata: Web sunucusu istenen kaynağı bulamadı.
Güvenlik konuları nedeniyle IIS genel bir hata döndürdü.

Olası bir nedeni sunucunun güvenlik yapılandırmasıdır. IIS 6.0 ve önceki sürümleri URLScan bilinen bir eklenti program şüpheli ve hatalı isteklerini filtrelemek için kullanılır. IIS 7.0 yerleşik istek filtreleme, aynı amaçla vardır. Her iki durumda da aşırı kısıtlayıcı istek filtrelemeyi Visual Studio sunucu hata ayıklamasından engelleyebilirsiniz.

Bu hata başka bir olası nedeni W3SVC hizmetini IIS için başlatılmamış ' dir. Bu hizmet hizmetler penceresinde (gri renkte) başlatıldığını kontrol edin (*services.msc*).

Bu hatanın olası çok sayıda ek nedenler vardır. Birkaç yaygın nedenlerinden dosya sisteminde IIS yüklemesi veya yapılandırma, web sitesi yapılandırması veya izinleri ile ilgili bir sorun içerir. Bir tarayıcı ile kaynağa erişmek deneyebilirsiniz. IIS nasıl yapılandırıldığına bağlı olarak, sunucu üzerinde yerel bir tarayıcı kullanın veya ayrıntılı hata iletisini almak için IIS hata günlüğünü inceleyin gerekebilir.

 IIS sorun giderme hakkında daha fazla bilgi için bkz. [IIS Yönetim ve Yönetim](/iis/manage/provisioning-and-managing-iis/iis-management-and-administration).

## <a name="see-also"></a>Ayrıca Bkz.
- [Hata: Web Sunucusu Kilitli ve DEBUG Fiilini Engelliyor](../debugger/error-the-web-server-has-been-locked-down-and-is-blocking-the-debug-verb.md)