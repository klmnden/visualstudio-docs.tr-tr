---
title: "Nasıl yapılır: Etkinlik günlüğü'nün | Microsoft Docs"
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSPackages, debugging
- VSPackages, troubleshooting
ms.assetid: bb3d3322-0e5e-4dd5-b93a-24d5fbcd2ffd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b0699e3a7ad4a56f7e102ca896359290cd7dbecb
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60053136"
---
# <a name="how-to-use-the-activity-log"></a>Nasıl yapılır: Etkinlik günlüğünü kullanma
VSPackage için etkinlik günlüğü iletileri yazabilirsiniz. Bu özellik, perakende ortamlarda VSPackages hata ayıklama için özellikle yararlıdır.

> [!TIP]
>  Etkinlik günlüğü her zaman açıktır. Visual Studio çalışırken bir arabellek genel yapılandırma bilgilerine sahip olan ilk 10 girişi yanı sıra, en son 100 girişleri tutar.

## <a name="to-write-an-entry-to-the-activity-log"></a>Etkinlik günlüğünün bir giriş yazmak için

1. Bu kodda Ekle <xref:Microsoft.VisualStudio.Shell.Package.Initialize%2A> yöntemi veya başka bir yöntem VSPackage Oluşturucusu hariç:

    ```csharp
    IVsActivityLog log = GetService(typeof(SVsActivityLog)) as IVsActivityLog;
    if (log == null) return;

    int hr = log.LogEntry((UInt32)__ACTIVITYLOG_ENTRYTYPE.ALE_INFORMATION,
        this.ToString(),
        string.Format(CultureInfo.CurrentCulture,
        "Called for: {0}", this.ToString()));
    ```

     Bu kod alır <xref:Microsoft.VisualStudio.Shell.Interop.SVsActivityLog> hizmet ve kendisine bıraktığı bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsActivityLog> arabirimi. <xref:Microsoft.VisualStudio.Shell.Interop.IVsActivityLog.LogEntry%2A> bilgilendirici bir giriş geçerli kültür bağlamını kullanarak etkinlik günlüğüne yazar.

2. VSPackage'ı (genellikle bir komut çağrılan veya bir pencere açılırsa olduğunda) yüklendiğinde, metin etkinlik günlüğüne yazılır.

## <a name="to-examine-the-activity-log"></a>Etkinlik günlüğünü incelemek için

1. Visual Studio ile çalışmak [/Log](../ide/reference/log-devenv-exe.md) ActivityLog.xml oturumunuz sırasında diske yazmak için komut satırı anahtarı.

2. Visual Studio kapatıldıktan sonra etkinlik günlüğü için Visual Studio veri alt klasörde bulabilirsiniz:

   <em>*% AppData %</em>\Microsoft\VisualStudio\\\<sürüm > \ActivityLog.xml*.

3. Etkinlik günlüğü herhangi bir metin düzenleyicisi ile açın. Tipik bir girişi şu şekildedir:

   ```
   Called for: Company.MyApp.MyAppPackage ...
   ```

## <a name="robust-programming"></a>Güçlü programlama

Etkinlik günlüğü bir hizmet olduğundan, etkinlik günlüğü VSPackage oluşturucuda kullanılamıyor.

Etkinlik günlüğü, yalnızca kendisine yazmadan önce almanız gerekir. Önbellek yok veya gelecekte kullanım için Etkinlik günlüğünü kaydedin.

## <a name="see-also"></a>Ayrıca bkz.

- [/ Log (devenv.exe)](../ide/reference/log-devenv-exe.md)
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsActivityLog>
- <xref:Microsoft.VisualStudio.Shell.Interop.__ACTIVITYLOG_ENTRYTYPE>
- [VSPackage Sorunlarını Giderme](../extensibility/troubleshooting-vspackages.md)
- [VSPackage’lar](../extensibility/internals/vspackages.md)
