---
title: 'Nasıl yapılır: .NET Framework çalışma zamanını belirtin. | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Profiling Tools, .NET Framework versions
- .NET Framework versions,profililng
ms.assetid: d39f3579-719a-4f47-a97d-5b4232fe4c64
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: f0179be3aa5ca55eef0854cc68a7e1287ac284f1
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66746419"
---
# <a name="how-to-specify-the-net-framework-runtime"></a>Nasıl yapılır: .NET Framework çalışma zamanını belirtme

.NET Framework 4'ın yayınlanmasıyla birlikte, uygulamaları, .NET Framework çalışma zamanı farklı sürümleri kullanılarak derlenmiş modüllerin oluşabilir. Varsayılan olarak, Visual Studio profil oluşturma araçları, uygulama tarafından yüklenen ilk çalışma zamanı profili. Bir uygulamaya Profil Oluşturucu ile başladığınızda ve profil oluşturucu zaten çalışan bir uygulamaya ekleme yaptığınızda profil için çalışma zamanı belirtebilirsiniz.

## <a name="to-specify-the-net-framework-run-time-to-profile-when-starting-an-application-with-the-profiler"></a>Profil Oluşturucu ile bir uygulama başlatma sırasında .NET Framework çalışma zamanı profili belirtmek için

1. İçinde **performans Gezgini**, performans oturumu sağ tıklayın, **özellikleri**ve ardından **Gelişmiş**.

     **Hedef CLR sürümü** liste kutusu görüntüler **otomatik** bilgisayarda yüklü olan .NET Framework çalışma zamanı sürümleri.

2. Aşağıdaki adımlardan birini uygulayın:

    - Profil oluşturmak istediğiniz CLR sürümünü tıklayın.

    - Tıklayın **otomatik** profilini uygulama tarafından yüklenen ilk sürümü.

## <a name="to-specify-the-net-framework-run-time-to-profile-when-attaching-the-profiler-to-an-application"></a>Bir uygulamaya profil oluşturucu iliştirme ne zaman .NET Framework çalışma zamanı profili belirtmek için

1. Üzerinde **Çözümle** menüsünde **Profiler**, ardından **Attach/Detach**.

2. Üzerinde **işleme iliştirmek Profiler** iletişim kutusunda, profil oluşturmak istediğiniz işleme tıklayın.

     **Hedef CLR sürümü** liste kutusu s **otomatik** bilgisayarda yüklü olan .NET Framework çalışma zamanı sürümleri.

3. Aşağıdaki adımlardan birini uygulayın:

    - Profil oluşturmak istediğiniz CLR sürümünü tıklayın.

    - Tıklayın **otomatik** uygulamaya profil oluşturucu ekler, yüklü sürümle profil için.