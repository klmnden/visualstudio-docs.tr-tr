---
title: "Nasıl yapılır: CD yüklemeleri için AutoStart'ı etkinleştirme | Microsoft Docs"
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
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
caps.latest.revision: 19
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: c4bd14060517793d28e24818a051df63efb8f0e0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68153779"
---
# <a name="how-to-enable-autostart-for-cd-installations"></a>Nasıl yapılır: CD Yüklemeleri için AutoStart'ı Etkinleştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Dağıtım yaparken bir [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] uygulama CD-ROM veya DVD-ROM gibi çıkarılabilir medya kullanarak etkinleştirebilirsiniz `AutoStart` böylece [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] uygulama ortam eklendiğinde otomatik olarak başlatılır.  
  
 `AutoStart` etkinleştirilebilir **Yayımla** sayfasının **Proje Tasarımcısı**.  
  
### <a name="to-enable-autostart"></a>AutoStart'ı etkinleştirmek için  
  
1. Seçili bir projeyle **Çözüm Gezgini**, **proje** menüsünü tıklatın **özellikleri**.  
  
2. Tıklayın **Yayımla** sekmesi.  
  
3. Tıklayın **seçenekleri** düğmesi.  
  
     **Yayımlama seçeneği** iletişim kutusu görüntülenir.  
  
4. Tıklayın **dağıtım**.  
  
5. Seçin **için CD yüklemeleri, CD takıldığında Kurulumu otomatik olarak Başlat** onay kutusu.  
  
     Uygulama yayımlandığında Autorun.inf dosya yayımlama konumuna kopyalanacak.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ClickOnce uygulamalarını yayımlama](../deployment/publishing-clickonce-applications.md)   
 [Nasıl yapılır: Yayımlama Sihirbazını Kullanarak ClickOnce Uygulaması Yayımlama](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)
