---
title: 'Nasıl yapılır: .NET Framework çalışma zamanını belirtin. | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Profiling Tools, .NET Framework versions
- .NET Framework versions,profililng
ms.assetid: d39f3579-719a-4f47-a97d-5b4232fe4c64
caps.latest.revision: 15
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 2f631e8639c1004fa2cb005da3b6c8bcb27f1a9b
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60076517"
---
# <a name="how-to-specify-the-net-framework-runtime"></a>Nasıl yapılır: .NET Framework çalışma zamanını belirtin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Sürümüyle [!INCLUDE[net_v40_long](../includes/net-v40-long-md.md)], uygulamalar oluşan farklı sürümleri kullanılarak derlenmiş modüllerin [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] çalışma zamanı. Varsayılan olarak, [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] profil oluşturma araçları, uygulama tarafından yüklenen ilk çalışma zamanı profili. Bir uygulamaya Profil Oluşturucu ile başladığınızda ve profil oluşturucu zaten çalışan bir uygulamaya ekleme yaptığınızda profil için çalışma zamanı belirtebilirsiniz.  
  
 **Gereksinimler**  
  
- [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
### <a name="to-specify-the-net-framework-run-time-to-profile-when-starting-an-application-with-the-profiler"></a>Profil Oluşturucu ile bir uygulama başlatma sırasında .NET Framework çalışma zamanı profili belirtmek için  
  
1. İçinde **performans Gezgini**, performans oturumu sağ tıklayın, **özellikleri**ve ardından **Gelişmiş**.  
  
     **Hedef CLR sürümü** liste kutusu görüntüler **otomatik** sürümleri [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] bilgisayarda yüklü çalışma zamanı.  
  
2. Aşağıdaki adımlardan birini uygulayın:  
  
    - Profil oluşturmak istediğiniz CLR sürümünü tıklayın.  
  
    - Tıklayın **otomatik** profilini uygulama tarafından yüklenen ilk sürümü.  
  
### <a name="to-specify-the-net-framework-run-time-to-profile-when-attaching-the-profiler-to-an-application"></a>Bir uygulamaya profil oluşturucu iliştirme ne zaman .NET Framework çalışma zamanı profili belirtmek için  
  
1. Analiz menüsünde için Profiler gelin ve iliştir/Ayır'ı tıklatın.  
  
2. İşlem iletişim kutusu için ekleme Profiler hakkında profil oluşturmak istediğiniz işleme tıklayın.  
  
     **Hedef CLR sürümü** liste kutusu s **otomatik** sürümleri [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] bilgisayarda yüklü çalışma zamanı.  
  
3. Aşağıdaki adımlardan birini uygulayın:  
  
    - Profil oluşturmak istediğiniz CLR sürümünü tıklayın.  
  
    - Tıklayın **otomatik** uygulamaya profil oluşturucu ekler, yüklü sürümle profil için.
