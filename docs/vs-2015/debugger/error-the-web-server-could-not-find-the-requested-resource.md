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
ms.openlocfilehash: 656ebd6f8b1e720afd129bca3d53712526fc914f
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57869198"
---
# <a name="error-the-web-server-could-not-find-the-requested-resource"></a>Hata: Web sunucusu istenen kaynağı bulamadı.
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Güvenlik konuları nedeniyle IIS genel bir hata döndürdü.  
  
 Olası bir nedeni sunucunun güvenlik yapılandırmasıdır. IIS 6.0 ve önceki sürümleri URLScan bilinen bir eklenti program şüpheli ve hatalı isteklerini filtrelemek için kullanılır. IIS 7.0 yerleşik istek filtreleme, aynı amaçla vardır. Her iki durumda da aşırı kısıtlayıcı istek filtrelemeyi Visual Studio sunucu hata ayıklamasından engelleyebilirsiniz.  
  
 Bu hata birçok olası nedenleri vardır. Birkaç yaygın nedenlerinden dosya sisteminde IIS yüklemesi veya yapılandırma, web sitesi yapılandırması veya izinleri ile ilgili bir sorun içerir. Bir tarayıcı ile kaynağa erişmek deneyebilirsiniz. IIS nasıl yapılandırdığına bağlı olarak sunucuda yerel bir tarayıcı kullanın veya ayrıntılı hata iletisini almak için IIS hata günlüğünü inceleyin gerekebilir.  
  
 IIS sorun giderme hakkında daha fazla bilgi için bkz. [IIS Yönetim ve Yönetim](http://go.microsoft.com/fwlink/?LinkId=255872).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [UrlScan güvenlik aracı](https://www.iis.net/downloads/microsoft/urlscan)   
 [Hata: Web Sunucusu Kilitli ve DEBUG Fiilini Engelliyor](../debugger/error-the-web-server-has-been-locked-down-and-is-blocking-the-debug-verb.md)
