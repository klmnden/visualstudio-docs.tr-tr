---
title: Hata ayıklayıcı Windows Workflow Foundation (eski) için devre dışı bırakma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
helpviewer_keywords:
- workflows, disabling debugger
- debugging workflows, disabling debugger
- workflow debugger, disabling
ms.assetid: 9da96d0e-f941-4fa9-a1a5-6bab50adfec9
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: e5065de4ec0217123f76eb23d32bcb0facd25dcc
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62823395"
---
# <a name="disabling-the-visual-studio-debugger-for-windows-workflow-foundation-legacy"></a>Windows Workflow Foundation için Visual Studio Hata Ayıklayıcısını Devre Dışı Bırakma (Eski)
Bu konu, devre dışı bırakmak açıklar [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] oluştururken yapılandırma dosyası kullanarak hata ayıklayıcı [!INCLUDE[wf](../includes/wf-md.md)] eski uygulamalarda [!INCLUDE[wfd1](../includes/wfd1-md.md)]. Eski kullanın [!INCLUDE[wfd2](../includes/wfd2-md.md)] hedeflemek gerektiğinde [!INCLUDE[netfx35_long](../includes/netfx35-long-md.md)] veya [!INCLUDE[vstecwinfx](../includes/vstecwinfx-md.md)].

 Varsayılan olarak, [!INCLUDE[vs_current_long](../includes/vs-current-long-md.md)] için hata ayıklayıcı [!INCLUDE[wf](../includes/wf-md.md)] bir ana bilgisayar işlemi için etkinleştirilir. İş akışı hata ayıklaması devre dışı bırakmak için açıkça bu "DisableWorkflowDebugging" giriş ekleyerek devre dışı bırakmalısınız  **\<anahtarlar >** öğesinde  **\<system.diagnostics >** ana bilgisayar yapılandırma dosyası bölümünü.

 Aşağıdaki örnek iş akışı hata ayıklaması devre dışı bırakmak için yapılandırma dosyası ana bilgisayarı değiştirmek nasıl gösterir.

```
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
   <system.diagnostics>
      <switches>
         <add name="DisableWorkflowDebugging" value="true"/>
      </switches>
   </system.diagnostics>
</configuration>
```

## <a name="see-also"></a>Ayrıca Bkz.
 [Windows Workflow Foundation (eski) için Visual Studio hata ayıklayıcısını çağırma](../workflow-designer/invoking-the-visual-studio-debugger-for-windows-workflow-foundation-legacy.md) [eski iş akışlarında hata ayıklama](../workflow-designer/debugging-legacy-workflows.md)