---
title: "Nasıl yapılır: Etkinlik günlüğü'nün | Microsoft Docs"
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- VSPackages, debugging
- VSPackages, troubleshooting
ms.assetid: bb3d3322-0e5e-4dd5-b93a-24d5fbcd2ffd
caps.latest.revision: 30
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d450e02d23159f186fd85bf1b687a2fb2c18e82a
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63432572"
---
# <a name="how-to-use-the-activity-log"></a>Nasıl yapılır: Etkinlik Günlüğünü Kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

VSPackage için etkinlik günlüğü iletileri yazabilirsiniz. Bu özellik, perakende ortamlarda VSPackages hata ayıklama için özellikle yararlıdır.  
  
> [!TIP]
> Etkinlik günlüğü her zaman açıktır. Visual Studio çalışırken bir arabellek genel yapılandırma bilgilerine sahip olan ilk on girişi yanı sıra yüz en son girdileri tutar.  
  
### <a name="to-write-an-entry-to-the-activity-log"></a>Etkinlik günlüğünün bir giriş yazmak için  
  
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
  
### <a name="to-examine-the-activity-log"></a>Etkinlik günlüğünü incelemek için  
  
1. Etkinlik günlüğü için Visual Studio veri alt Bul: *% AppData %* \Microsoft\VisualStudio\14.0\ActivityLog.XML...  
  
2. Etkinlik günlüğü herhangi bir metin düzenleyicisi ile açın. Tipik bir girişi şu şekildedir:  
  
    ```  
    Called for: Company.MyApp.MyAppPackage ...  
    ```  
  
## <a name="robust-programming"></a>Güçlü Programlama  
 Etkinlik günlüğü bir hizmet olduğundan, etkinlik günlüğü VSPackage oluşturucuda kullanılamıyor.  
  
 Etkinlik günlüğü, yalnızca kendisine yazmadan önce almanız gerekir. Önbellek yok veya gelecekte kullanım için Etkinlik günlüğünü kaydedin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsActivityLog>   
 <xref:Microsoft.VisualStudio.Shell.Interop.__ACTIVITYLOG_ENTRYTYPE>   
 [VSPackage sorunlarını giderme](../extensibility/troubleshooting-vspackages.md)   
 [VSPackage’lar](../extensibility/internals/vspackages.md)
