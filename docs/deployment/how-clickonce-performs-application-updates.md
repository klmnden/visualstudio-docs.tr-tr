---
title: ClickOnce uygulama güncelleştirmelerini nasıl gerçekleştirir | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- updates, ClickOnce
- ClickOnce deployment, updates
- deploying applications [ClickOnce], application updates
ms.assetid: d54313c2-cf0c-420d-b151-99953a95f0bb
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 5fc3414660f206aa8f83179e61ed9aa2dcc0098b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53845609"
---
# <a name="how-clickonce-performs-application-updates"></a>ClickOnce uygulama güncelleştirmelerini nasıl gerçekleştirir
ClickOnce, uygulama dosyalarını güncelleştirmek karar vermek için bir uygulamanın dağıtım bildiriminde belirtilen dosya sürümü bilgilerini kullanır. Bir güncelleştirme başladıktan sonra ClickOnce, adında bir teknik kullanır. *dosya düzeltme eki uygulama* yedekli uygulama dosyalarının yüklenmesini önlemek için.  
  
## <a name="file-patching"></a>Dosya düzeltme eki uygulama  
 Dosyaları değiştirmediğiniz sürece bir uygulamayı güncelleştirdiğinizde, ClickOnce tüm dosyalar için uygulamanın yeni sürümünü karşıdan yüklemez. Bunun yerine, yeni sürüm için bildirim imzaları geçerli uygulama için uygulama bildiriminde belirtilen dosyalar karma imzalarını karşılaştırır. Bir dosyanın imzaları farklı ise, ClickOnce yeni sürümü yükler. İmzalar eşleşirse, dosyanın bir sürümünden sonraki değiştirilmemiştir. Bu durumda, ClickOnce, var olan dosyayı kopyalar ve uygulamayı yeni sürümünde kullanır. Bu yaklaşım ClickOnce yalnızca bir veya iki dosyalar değiştirilmiş olsa bile tüm uygulamayı yeniden indirmek zorunda kalmasını önler.  
  
 Düzeltme eki dosyası da çalışır yüklenen derlemeler için kullanarak isteğe bağlı olarak <xref:System.Deployment.Application.ApplicationDeployment.DownloadFileGroup%2A> ve <xref:System.Deployment.Application.ApplicationDeployment.DownloadFileGroupAsync%2A> yöntemleri.  
  
 Uygulamanızı derlemek için Visual Studio kullanıyorsanız, tüm projeyi yeniden her tüm dosyalar için yeni karma imzaları oluşturur. Bu durumda, yalnızca birkaç derlemeleri değişmiş olabilir ancak tüm derlemeler istemciye indirilir.  
  
 Dosya düzeltme eki uygulama, verileri olarak işaretlenmiş ve veri dizininde depolanan dosyalar için çalışmaz. Bu, dosyanın karması imzasını bağımsız olarak daima yüklenir. Veri dizini hakkında daha fazla bilgi için bkz. [ClickOnce uygulamalarında yerel ve uzak veri erişim](../deployment/accessing-local-and-remote-data-in-clickonce-applications.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [ClickOnce güncelleştirme stratejisini seçin](../deployment/choosing-a-clickonce-update-strategy.md)   
 [ClickOnce dağıtım stratejisini seçin](../deployment/choosing-a-clickonce-deployment-strategy.md)