---
title: Durum Kalıcılık desteği | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: devlang-csharp
ms.topic: conceptual
helpviewer_keywords:
- state persistence, managed package framework support
- managed package framework, state persistence support
- state, persistence
ms.assetid: d25866f2-8d1f-477f-8aa5-3af3fbbf6e97
caps.latest.revision: 15
manager: jillfra
ms.openlocfilehash: 6dc542d2e410b79a21e436a1881c06bd3cc4eef8
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54801814"
---
# <a name="support-for-state-persistence"></a>Durum Kalıcılık desteği
[!INCLUDE[vsprvs](../includes/vsprvs-md.md)] ortak nesneleri durumunu koruyabilir. Örneğin, çözüm ve proje özellikleri için kaydedilir ve çözüm ve proje dosyalarından geri. Kullanıcı ayarları için dışarı ve ayarları dosyalarından içeri aktarıldı.  
  
 VSPackage'ları genellikle sistem kayıt defterinde veya uygulama verileri klasörü geçerli bir kullanıcı veya bilgisayar için yerel depolama kullanır. Tam sayılar ve dizeler gibi depolama için az miktarda alan gerektiren değerleri, genellikle sistem kayıt defterinde depolanır. Bit eşlemleri gibi depolama için çok fazla alan gerektiren değerleri bir dosyaya kaydedilir. Dosya yolunu kendi sistem kayıt defterinde kaydedilebilir. Kalıcılık mekanizması, yerel depolama erişim izni olması gerekir.  
  
## <a name="support-for-locating-local-storage"></a>Yerel depolama bulma desteği  
 <xref:Microsoft.VisualStudio.Shell.Package> Sınıfı, geçerli kullanıcı veya bilgisayar için sistem kayıt defteri veya uygulama verileri klasörü durum bilgilerini bulmak için destek sağlar.  
  
 <xref:Microsoft.VisualStudio.Shell.Package.ApplicationRegistryRoot%2A>  
 Yerel bilgisayarın kayıt defteri kökü için yolunu döndürür [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], örneğin, HKEY_LOCAL_MACHINE\Software\Microsoft\VisualStudio\8.0Exp.  
  
 Yerel kayıt defteri kökü elde edilen <xref:Microsoft.VisualStudio.Shell.Interop.SVsShell> hizmeti. Bu kullanılamıyorsa öğesinden alınır <xref:Microsoft.VisualStudio.Shell.DefaultRegistryRootAttribute> VSPackage özniteliği.  
  
 <xref:Microsoft.VisualStudio.Shell.Package.UserRegistryRoot%2A>  
 Geçerli kullanıcının (bilgisayar) başına yolunu döndürür için kayıt defteri kökü [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], örneğin, HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0Exp.  
  
 Yerel kayıt defteri kökü elde edilen <xref:Microsoft.VisualStudio.Shell.Interop.SVsShell> hizmeti. Bu kullanılamıyorsa VSPackage DefaultLocalRegistryRoot özniteliğinden elde edilir.  
  
 <xref:Microsoft.VisualStudio.Shell.Package.UserDataPath%2A>  
 İçin ortak bir depo görevi gören bir dizinin yolunu döndürür [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] C:\Documents ve ayarları geçerli Dolaşım kullanıcı için veri\\*YourAccountName*\Application Data\Microsoft\ VisualStudio\8.0Exp.  
  
 <xref:Microsoft.VisualStudio.Shell.Package.UserLocalDataPath%2A>  
 İçin ortak bir depo görevi gören bir dizinin yolunu döndürür [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] geçerli gezici olmayan, örneğin, C:\Documents ve kullanıcı ayarları için veri\\*YourAccountName*\Local Data\Microsoft\VisualStudio\8.0Exp.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPackage'ı durumu](../misc/vspackage-state.md)