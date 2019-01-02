---
title: "Nasıl Yapılır: CD yüklemeleri için AutoStart'ı etkinleştirme | Microsoft Docs"
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, AutoStart
- ClickOnce deployment, installation on CD or DVD
- deploying applications [ClickOnce], installation on CD or DVD
ms.assetid: caaec619-900c-4790-90e3-8c91f5347635
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 35a6d98a476a8a9612cb5bfb80e7fa8b2f00c4ed
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53864027"
---
# <a name="how-to-enable-autostart-for-cd-installations"></a>Nasıl Yapılır: CD yüklemeleri için AutoStart'ı etkinleştir
Dağıtım yaparken bir [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama CD-ROM veya DVD-ROM gibi çıkarılabilir medya kullanarak etkinleştirebilirsiniz `AutoStart` böylece [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] uygulama ortam eklendiğinde otomatik olarak başlatılır.  
  
 `AutoStart` etkinleştirilebilir **Yayımla** sayfasının **Proje Tasarımcısı**.  
  
### <a name="to-enable-autostart"></a>AutoStart'ı etkinleştirmek için  
  
1.  Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünü tıklatın **özellikleri**.  
  
2.  Tıklayın **Yayımla** sekmesi.  
  
3.  Tıklayın **seçenekleri** düğmesi.  
  
     **Yayımlama seçeneği** iletişim kutusu görüntülenir.  
  
4.  Tıklayın **dağıtım**.  
  
5.  Seçin **için CD yüklemeleri, CD takıldığında Kurulumu otomatik olarak Başlat** onay kutusu.  
  
     Bir *Autorun.inf* dosya uygulama yayımlandığında yayımlama konumuna kopyalanır.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)   
 [Nasıl yapılır: Yayımlama Sihirbazını kullanarak ClickOnce uygulaması yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)