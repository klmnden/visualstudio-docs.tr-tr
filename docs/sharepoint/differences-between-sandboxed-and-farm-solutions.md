---
title: Korumalı arasındaki farklar ve Grup çözümleri | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, sandboxed solutions
- sandboxed solutions [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, farm solutions
- farm solutions [SharePoint development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 49dcd021e3f04d78af9d0ff50e7001dedcc73297
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54867864"
---
# <a name="differences-between-sandboxed-and-farm-solutions"></a>Korumalı arasındaki farklar ve Grup çözümleri
  Bir SharePoint çözüm derlediğinizde, SharePoint sunucusuna dağıtır ve hata ayıklamak için bir hata ayıklayıcı ekler. Çözüm hata ayıklamak için kullanılan işlem Korumalı çözüm özelliğinin ayarına bağlıdır: Korumalı çözüm veya Grup çözümü.  
  
 Daha fazla bilgi için [korumalı çözümle ilgili konular](../sharepoint/sandboxed-solution-considerations.md).  
  
## <a name="farm-solutions"></a>Küme çözümleri
 IIS çalışan işlemi (W3WP.exe) barındırılan, küme çözümleri, tüm Grup etkileyebilecek kodu çalıştırın. Korumalı çözüm özelliği "Grup çözümü" olarak ayarlanmış bir SharePoint projesi hata ayıklaması yaparken, SharePoint çeker veya IIS çalışan işlemi tarafından kilitlenmiş dosyaları serbest bırakmak için özelliği dağıtır önce sistemin IIS uygulama havuzunu geri dönüştürür. Yalnızca SharePoint projenin site URL'si tanıtıcısıyla IIS uygulama havuzu geri dönüştürülmeden.  
  
## <a name="sandboxed-solutions"></a>Korumalı alana alınan çözümler
 SharePoint kullanıcı kodu çözüm çalışan işlemindeki (SPUCWorkerProcess.exe) barındırılan, korumalı çözümler site koleksiyonu çözümü, yalnızca etkileyebilecek kodu çalıştırın. Korumalı çözümler IIS çalışan işlemindeki çalıştırmayın çünkü IIS uygulama havuzu ya da IIS sunucusunu yeniden başlatmanız gerekir. [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] hata ayıklayıcı, denetimleri ve otomatik olarak SharePoint SPUserCodeV4 hizmetinde tetikleyen SPUCWorkerProcess işlem ekler. Çözüm en son sürümünü yüklemek için Geri Dönüşüm SPUCWorkerProcess işlemi için gerekli değildir.  
  
## <a name="either-type-of-solution"></a>Çözüm ya da türü
 Her iki çözüm türü ile [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] da tarayıcıya istemci tarafı komut dosyası hata ayıklamayı etkinleştirmek için hata ayıklayıcı ekler. [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] hata ayıklama altyapısı bu amaç için betik kullanır. Betik hata ayıklamasını etkinleştirmek için istendiğinde varsayılan tarayıcı ayarlarınızı değiştirmeniz gerekir.  
  
 [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] hata ayıklayıcı, geçerli site çalışan yalnızca W3WP veya SPUCWorkerProcess işlemleri için ekler. [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] Ayrıca yönetilen COM Plus ve iş akışı hata ayıklama altyapıları ekler.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint çözümlerinde hata ayıklama](../sharepoint/debugging-sharepoint-solutions.md)   
 [Derleme ve SharePoint çözümlerinde hata ayıklama](../sharepoint/building-and-debugging-sharepoint-solutions.md)   
 [Korumalı çözümle ilgili konular](../sharepoint/sandboxed-solution-considerations.md)  
