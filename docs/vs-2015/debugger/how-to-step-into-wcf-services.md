---
title: 'Nasıl yapılır: WCF hizmetleri içine Adımlama | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugging, WCF
- WCF, debugging
ms.assetid: 9893ad01-54af-499f-85a6-9d1cfe6eb640
caps.latest.revision: 27
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 951d5f39fbf3929d094cc18de5fe108b46753b09
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60056451"
---
# <a name="how-to-step-into-wcf-services"></a>Nasıl yapılır: WCF hizmetleri içine Adımlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İçinde [!INCLUDE[vs_dev11_long](../includes/vs-dev11-long-md.md)], bir WCF hizmetinde geçebilirsiniz. WCF hizmeti aynı ise [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] çözüm istemci olarak WCF hizmeti içinde kesme noktaları isabet.  
  
 Çalışmak için atlamak için hata ayıklama app.config veya Web.config dosyasında etkin olması gerekir. Hata ayıklamayı ve WCF hizmetleri içine Adımlama sınırlamalar hakkında bilgi için [WCE hata ayıklama sınırlamaları](../debugger/limitations-on-wcf-debugging.md).  
  
### <a name="to-step-into-a-wcf-service"></a>Bir WCF Hizmeti adımlamak için  
  
1. Oluşturma bir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] WCF istemcisi ve WCF Hizmeti projeleri içeren çözüm.  
  
2. Çözüm Gezgini'nde, WCF istemcisi projeye sağ tıklayın ve ardından **başlangıç projesi olarak ayarla**.  
  
3. App.config veya web.config dosyasında hata ayıklamayı etkinleştirin. Daha fazla bilgi için [WCE hata ayıklama sınırlamaları](../debugger/limitations-on-wcf-debugging.md).  
  
4. İstemci projesindeki adımlamaya başlamak istediğiniz konumda bir kesme noktası ayarlayın. Genellikle, bu yalnızca WCF Hizmeti çağrısından önce olacaktır.  
  
5. Kesme noktasına kadar çalıştırın, ardından Adımlama başlayın. Hata ayıklayıcı hizmette otomatik olarak adım adım anlatır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [WCF hizmetlerinde hata ayıklama](../debugger/debugging-wcf-services.md)   
 [WCE hata ayıklamasında sınırlamalar](../debugger/limitations-on-wcf-debugging.md)   
 [Nasıl yapılır: Kendini Barındıran WCF Hizmetinde Hata Ayıklama](../debugger/how-to-debug-a-self-hosted-wcf-service.md)
