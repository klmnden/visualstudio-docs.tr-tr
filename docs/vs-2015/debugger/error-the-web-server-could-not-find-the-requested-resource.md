---
title: 'Hata: Web sunucusu istenen kaynağı bulamadı. | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugger, Web application errors
ms.assetid: 1ceeaf30-918c-42bb-ace1-96944530fef3
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 84a264aee56a179934f0ad7ad2b8a26fd69b697b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54800004"
---
# <a name="error-the-web-server-could-not-find-the-requested-resource"></a>Hata: Web sunucusu istenen kaynağı bulamadı.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Güvenlik konuları nedeniyle IIS genel bir hata döndürdü.  
  
 Olası bir nedeni sunucunun güvenlik yapılandırmasıdır. IIS 6.0 ve önceki sürümleri URLScan bilinen bir eklenti program şüpheli ve hatalı isteklerini filtrelemek için kullanılır. IIS 7.0 yerleşik istek filtreleme, aynı amaçla vardır. Her iki durumda da aşırı kısıtlayıcı istek filtrelemeyi Visual Studio sunucu hata ayıklamasından engelleyebilirsiniz.  
  
 Bu hata birçok olası nedenleri vardır. Birkaç yaygın nedenlerinden dosya sisteminde IIS yüklemesi veya yapılandırma, web sitesi yapılandırması veya izinleri ile ilgili bir sorun içerir. Bir tarayıcı ile kaynağa erişmek deneyebilirsiniz. IIS nasıl yapılandırdığına bağlı olarak sunucuda yerel bir tarayıcı kullanın veya ayrıntılı hata iletisini almak için IIS hata günlüğünü inceleyin gerekebilir.  
  
 IIS sorun giderme hakkında daha fazla bilgi için bkz. [IIS Yönetim ve Yönetim](http://go.microsoft.com/fwlink/?LinkId=255872).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [UrlScan güvenlik aracı](http://www.microsoft.com/technet/security/tools/urlscan.mspx)   
 [Hata: Web Sunucusu Kilitli ve DEBUG Fiilini Engelliyor](../debugger/error-the-web-server-has-been-locked-down-and-is-blocking-the-debug-verb.md)
