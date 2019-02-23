---
title: 'Nasıl yapılır: WCF hizmetleri içine Adımlama | Microsoft Docs'
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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0fe025ed3050f25ec53175c543adfaf7cb48c506
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56689817"
---
# <a name="how-to-step-into-wcf-services"></a>Nasıl yapılır: WCF hizmetleri içine Adımlama
İçinde [!INCLUDE[vs_dev11_long](../data-tools/includes/vs_dev11_long_md.md)], bir WCF hizmetinde geçebilirsiniz. WCF hizmeti aynı ise [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] çözüm istemci olarak WCF hizmeti içinde kesme noktaları isabet.

 Çalışmak için atlamak için hata ayıklama app.config veya Web.config dosyasında etkin olması gerekir. Hata ayıklamayı ve WCF hizmetleri içine Adımlama sınırlamalar hakkında bilgi için [WCE hata ayıklama sınırlamaları](../debugger/limitations-on-wcf-debugging.md).

### <a name="to-step-into-a-wcf-service"></a>Bir WCF Hizmeti adımlamak için

1. Oluşturma bir [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] WCF istemcisi ve WCF Hizmeti projeleri içeren çözüm.

2. Çözüm Gezgini'nde, WCF istemcisi projeye sağ tıklayın ve ardından **başlangıç projesi olarak ayarla**.

3. App.config veya web.config dosyasında hata ayıklamayı etkinleştirin. Daha fazla bilgi için [WCE hata ayıklama sınırlamaları](../debugger/limitations-on-wcf-debugging.md).

4. İstemci projesindeki adımlamaya başlamak istediğiniz konumda bir kesme noktası ayarlayın. Genellikle, bu yalnızca WCF Hizmeti çağrısından önce olacaktır.

5. Kesme noktasına kadar çalıştırın, ardından Adımlama başlayın. Hata ayıklayıcı hizmette otomatik olarak adım adım anlatır.

## <a name="see-also"></a>Ayrıca Bkz.
- [WCF Hizmetlerinde Hata Ayıklama](../debugger/debugging-wcf-services.md)
- [WCE Hata Ayıklama Sınırlamaları](../debugger/limitations-on-wcf-debugging.md)
- [Nasıl yapılır: Kendini Barındıran WCF Hizmetinde Hata Ayıklama](../debugger/how-to-debug-a-self-hosted-wcf-service.md)