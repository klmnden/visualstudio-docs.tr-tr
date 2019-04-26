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
ms.openlocfilehash: 9563cafa4895f89253b4073d788240806a86fa2a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62561084"
---
# <a name="access-is-denied"></a>Erişim reddedildi
Bir betik konağı geçerli sayfanın dışında bir kaynaktan verilere erişmeye çalıştı. Internet Explorer ve diğer tarayıcılar tarafından izlenen bir aynı çıkış noktası İlkesi, betiklerin yalnızca şema, konak ve bağlantı noktası geçerli sayfasının URL'si ile kaynaklardan veri erişmesine izin verir.  
  
 Örneğin, geçerli sayfa ise `https://employees.mycompany.com`, aşağıdaki URL'lerden verilere erişemezsiniz:  
  
- `http://data.contoso.com`, HTTPS yerine HTTP kullandığından.  
  
- `https://somedatasource.com`, farklı bir etki alanı olduğu için.  
  
- `https://employees.mycompany.com:8888`, farklı bir bağlantı noktasını kullandığından.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Çağırmaya çalıştığınız API JSONP veya güvenli bir şekilde çıkış noktaları arası komut dosyası izin veren iki yaklaşım olan CORS destekleyip desteklemediğini araştırın.  
  
- REST API'sini çağırmak çalışıyorsanız, bu çağrı, sunucu tarafı kodu yeniden düzenleyin ve ardından, istemci tarafı betikleri için yeni bir REST uç noktasını kullanıma sunar.  
  
     Ek bilgi için aynı çıkış noktası İlkesi, JSONP ve CORS ile ilgili çevrimiçi belgeleri arayın.
