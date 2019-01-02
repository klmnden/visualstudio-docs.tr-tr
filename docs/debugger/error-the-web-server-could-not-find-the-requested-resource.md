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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 798e0892fc78b4ff8f8eb8ed03ee788e4f8f5b25
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53866549"
---
# <a name="error-the-web-server-could-not-find-the-requested-resource"></a>Hata: Web sunucusu istenen kaynağı bulamadı.
Güvenlik konuları nedeniyle IIS genel bir hata döndürdü.  

Olası bir nedeni sunucunun güvenlik yapılandırmasıdır. IIS 6.0 ve önceki sürümleri URLScan bilinen bir eklenti program şüpheli ve hatalı isteklerini filtrelemek için kullanılır. IIS 7.0 yerleşik istek filtreleme, aynı amaçla vardır. Her iki durumda da aşırı kısıtlayıcı istek filtrelemeyi Visual Studio sunucu hata ayıklamasından engelleyebilirsiniz.  

Bu hata başka bir olası nedeni W3SVC hizmetini IIS için başlatılmamış ' dir. Bu hizmet hizmetler penceresinde (gri renkte) başlatıldığını kontrol edin (*services.msc*).

Bu hatanın olası çok sayıda ek nedenler vardır. Birkaç yaygın nedenlerinden dosya sisteminde IIS yüklemesi veya yapılandırma, web sitesi yapılandırması veya izinleri ile ilgili bir sorun içerir. Bir tarayıcı ile kaynağa erişmek deneyebilirsiniz. IIS nasıl yapılandırıldığına bağlı olarak, sunucu üzerinde yerel bir tarayıcı kullanın veya ayrıntılı hata iletisini almak için IIS hata günlüğünü inceleyin gerekebilir.  
  
 IIS sorun giderme hakkında daha fazla bilgi için bkz. [IIS Yönetim ve Yönetim](/iis/manage/provisioning-and-managing-iis/iis-management-and-administration).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata: Web sunucusu kilitli ve DEBUG fiilini engelliyor](../debugger/error-the-web-server-has-been-locked-down-and-is-blocking-the-debug-verb.md)