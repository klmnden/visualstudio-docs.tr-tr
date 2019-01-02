---
title: 'Nasıl Yapılır: WCF hizmetleri içine Adımlama | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging, WCF
- WCF, debugging
ms.assetid: 9893ad01-54af-499f-85a6-9d1cfe6eb640
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f361369aef97aaa894a1a1929149356d3177cc3f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53890741"
---
# <a name="how-to-step-into-wcf-services"></a>Nasıl Yapılır: WCF hizmetleri içine Adımlama
İçinde [!INCLUDE[vs_dev11_long](../data-tools/includes/vs_dev11_long_md.md)], bir WCF hizmetinde geçebilirsiniz. WCF hizmeti aynı ise [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] çözüm istemci olarak WCF hizmeti içinde kesme noktaları isabet.  
  
 Çalışmak için atlamak için hata ayıklama app.config veya Web.config dosyasında etkin olması gerekir. Hata ayıklamayı ve WCF hizmetleri içine Adımlama sınırlamalar hakkında bilgi için [WCE hata ayıklama sınırlamaları](../debugger/limitations-on-wcf-debugging.md).  
  
### <a name="to-step-into-a-wcf-service"></a>Bir WCF Hizmeti adımlamak için  
  
1. Oluşturma bir [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] WCF istemcisi ve WCF Hizmeti projeleri içeren çözüm.  
  
2. Çözüm Gezgini'nde, WCF istemcisi projeye sağ tıklayın ve ardından **başlangıç projesi olarak ayarla**.  
  
3. App.config veya web.config dosyasında hata ayıklamayı etkinleştirin. Daha fazla bilgi için [WCE hata ayıklama sınırlamaları](../debugger/limitations-on-wcf-debugging.md).  
  
4. İstemci projesindeki adımlamaya başlamak istediğiniz konumda bir kesme noktası ayarlayın. Genellikle, bu yalnızca WCF Hizmeti çağrısından önce olacaktır.  
  
5. Kesme noktasına kadar çalıştırın, ardından Adımlama başlayın. Hata ayıklayıcı hizmette otomatik olarak adım adım anlatır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [WCF hizmetlerinde hata ayıklama](../debugger/debugging-wcf-services.md)   
 [WCE hata ayıklamasında sınırlamalar](../debugger/limitations-on-wcf-debugging.md)   
 [Nasıl yapılır: Kendini barındıran WCF hizmetinde hata ayıklama](../debugger/how-to-debug-a-self-hosted-wcf-service.md)