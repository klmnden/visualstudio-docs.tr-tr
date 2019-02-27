---
title: Erişim reddedildi | Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: 8a512060-d744-47af-a83e-4ba42ea2c5b2
author: mikejo5000
ms.author: mikejo
ms.openlocfilehash: 75f1bb08031769c06f7d94d4f8c120496fffc02d
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56843759"
---
# <a name="access-is-denied"></a>Erişim reddedildi
Bir betik konağı geçerli sayfanın dışında bir kaynaktan verilere erişmeye çalıştı. Internet Explorer ve diğer tarayıcılar tarafından izlenen bir aynı çıkış noktası İlkesi, betiklerin yalnızca şema, konak ve bağlantı noktası geçerli sayfasının URL'si ile kaynaklardan veri erişmesine izin verir.  
  
 Örneğin, geçerli sayfa ise `https://employees.mycompany.com`, aşağıdaki URL'lerden verilere erişemezsiniz:  
  
-   `http://data.contoso.com`, HTTPS yerine HTTP kullandığından.  
  
-   `https://somedatasource.com`, farklı bir etki alanı olduğu için.  
  
-   `https://employees.mycompany.com:8888`, farklı bir bağlantı noktasını kullandığından.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Çağırmaya çalıştığınız API JSONP veya güvenli bir şekilde çıkış noktaları arası komut dosyası izin veren iki yaklaşım olan CORS destekleyip desteklemediğini araştırın.  
  
-   REST API'sini çağırmak çalışıyorsanız, bu çağrı, sunucu tarafı kodu yeniden düzenleyin ve ardından, istemci tarafı betikleri için yeni bir REST uç noktasını kullanıma sunar.  
  
     Ek bilgi için aynı çıkış noktası İlkesi, JSONP ve CORS ile ilgili çevrimiçi belgeleri arayın.
