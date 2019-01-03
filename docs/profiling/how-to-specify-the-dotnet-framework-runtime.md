---
title: 'Nasıl Yapılır: .NET Framework çalışma zamanını belirtin. | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Profiling Tools, .NET Framework versions
- .NET Framework versions,profililng
ms.assetid: d39f3579-719a-4f47-a97d-5b4232fe4c64
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 6baa0e37acb4ba24d0622ad27fe84c47e84da59d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53911019"
---
# <a name="how-to-specify-the-net-framework-runtime"></a>Nasıl Yapılır: .NET Framework çalışma zamanını belirtme

Sürümüyle [!INCLUDE[net_v40_long](../code-quality/includes/net_v40_long_md.md)], uygulamalar oluşan farklı sürümleri kullanılarak derlenmiş modüllerin [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] çalışma zamanı. Varsayılan olarak, Visual Studio profil oluşturma araçları, uygulama tarafından yüklenen ilk çalışma zamanı profili. Bir uygulamaya Profil Oluşturucu ile başladığınızda ve profil oluşturucu zaten çalışan bir uygulamaya ekleme yaptığınızda profil için çalışma zamanı belirtebilirsiniz.

## <a name="to-specify-the-net-framework-run-time-to-profile-when-starting-an-application-with-the-profiler"></a>Profil Oluşturucu ile bir uygulama başlatma sırasında .NET Framework çalışma zamanı profili belirtmek için

1. İçinde **performans Gezgini**, performans oturumu sağ tıklayın, **özellikleri**ve ardından **Gelişmiş**.

     **Hedef CLR sürümü** liste kutusu görüntüler **otomatik** sürümleri [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] bilgisayarda yüklü çalışma zamanı.

2. Aşağıdaki adımlardan birini uygulayın:

    - Profil oluşturmak istediğiniz CLR sürümünü tıklayın.

    - Tıklayın **otomatik** profilini uygulama tarafından yüklenen ilk sürümü.

## <a name="to-specify-the-net-framework-run-time-to-profile-when-attaching-the-profiler-to-an-application"></a>Bir uygulamaya profil oluşturucu iliştirme ne zaman .NET Framework çalışma zamanı profili belirtmek için

1. Üzerinde **Çözümle** menüsünde **Profiler**, ardından **Attach/Detach**.

2. Üzerinde **işleme iliştirmek Profiler** iletişim kutusunda, profil oluşturmak istediğiniz işleme tıklayın.

     **Hedef CLR sürümü** liste kutusu s **otomatik** sürümleri [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] bilgisayarda yüklü çalışma zamanı.

3. Aşağıdaki adımlardan birini uygulayın:

    - Profil oluşturmak istediğiniz CLR sürümünü tıklayın.

    - Tıklayın **otomatik** uygulamaya profil oluşturucu ekler, yüklü sürümle profil için.