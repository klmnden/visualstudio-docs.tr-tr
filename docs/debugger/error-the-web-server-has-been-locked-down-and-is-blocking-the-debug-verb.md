---
title: 'Hata: Web sunucusu kilitli ve DEBUG fiilini engelliyor | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.webdbg_debug_verb_blocked
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
ms.openlocfilehash: 277619cb89003aea9dca58678f251f2f21826046
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55026599"
---
# <a name="error-the-web-server-has-been-locked-down-and-is-blocking-the-debug-verb"></a>Hata: Web sunucusu kilitli ve DEBUG fiilini engelliyor
Bir Web uygulaması veya XML Web hizmeti içine Adımlama, IIS Kilitleme aracını çalıştırın ve URLScan yüklü ve etkin olduğundan başarısız oldu. Bu durum, IIS DEBUG fiilini almasını engeller.  
  
 URLScan IIS Web sitesi yöneticilerinin gereksiz özelliklerini Kapat ve sunucu işleyecek HTTP istek türlerini kısıtlamak olanağı vermek için IIS Kilitleme Aracı ile birlikte çalışan bir güvenlik aracıdır. URLScan güvenlik aracı, belirli HTTP isteklerini engelleyerek, sunucuya ulaşmadan ve zarar görmesine neden zararlı olabilecek istekleri engeller.  
  
 Uygulamanızı IIS 6.0, Windows Server 2003 çalıştırıyorsa, çünkü IIS 6.0 aynı işlevselliği sağlar, IIS Kilitleme aracını çalıştırmamanız.  
  
### <a name="to-enable-debugging-on-a-web-server-with-urlscan-installed"></a>Bir Web sunucusunda yüklü URLScan ile hata ayıklamayı etkinleştirmek için  
  
1.  Urlscan.ini dosyasını bulun. Normalde, şuna benzer bir dizinde bulacaksınız:  
  
     C:\WINNT\System32\Inetsrv\urlscan  
  
2.  Dosyanın bir kopyasını oluşturun ve adlandırın **Urlscan.old**.  
  
3.  Özgün kopyasını Urlscan.ini dosyasını Not Defteri'nde veya tercih ettiğiniz metin düzenleyiciyi kullanarak açın.  
  
4.  URLScan.ini içinde [AllowVerbs] bölümünü bulun. Hata ayıklama [AllowVerbs] bölümüne ekleyin. Görürseniz; [AllowVerbs] bölümünde hata AYIKLAMAK için noktalı fiili açıklamasını kaldırın.  
  
5.  [DenyVerbs] bölümünü bulun. Hata ayıklama [DenyVerbs] bölümünde görünüyorsa, bunu kaldırın.  
  
6.  Dosyayı kaydedin.  
  
7.  Sunucuyu yeniden başlatın veya IIS'yi yeniden başlatın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Web Uygulamalarında Hata Ayıklama: Hatalar ve sorun giderme](../debugger/debugging-web-applications-errors-and-troubleshooting.md)   
 [Hata: Web Sunucusu İstenen Kaynağı Bulamadı](../debugger/error-the-web-server-could-not-find-the-requested-resource.md)