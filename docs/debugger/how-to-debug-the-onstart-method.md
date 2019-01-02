---
title: 'Nasıl Yapılır: OnStart metodunda hata ayıklama | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- OnStart method
- debugging [Visual Studio], Windows services
- debugging managed code, OnStart method
- debugging Windows Services applications, OnStart method
- Windows Service applications, debugging
ms.assetid: b06b5d65-424b-490f-bf58-97583cd7006a
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 53106b0d933c25d69ecd0b455b89f68c09b9a169
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53822955"
---
# <a name="how-to-debug-the-onstart-method"></a>Nasıl Yapılır: OnStart metodunda hata ayıklama
Bir Windows hizmeti, hizmete ve hata ayıklayıcı hizmet işlemine iliştirme ayıklayabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Windows hizmet uygulamalarında hata ayıklama](/dotnet/framework/windows-services/how-to-debug-windows-service-applications). Ancak, hata ayıklamak için <xref:System.ServiceProcess.ServiceBase.OnStart%2A?displayProperty=fullName> yöntemi bir Windows hizmetinin ayıklayıcısından yöntemi içinde başlatmak gerekir.  
  
1.  Bir çağrı ekleyin <xref:System.Diagnostics.Debugger.Launch%2A> başındaki `OnStart()`yöntemi.  
  
    ```csharp  
    protected override void OnStart(string[] args)  
    {  
        System.Diagnostics.Debugger.Launch();  
     }  
    ```  
  
2.  Hizmeti Başlat (kullanabilirsiniz `net start`, ya da başlatın **Hizmetleri** pencere).  
  
     Bir iletişim kutusu aşağıdaki gibi görmeniz gerekir:  
  
     ![OnStartDebug](../debugger/media/onstartdebug.png "OnStartDebug")  
  
3.  Seçin **Evet, hata ayıklama \<hizmet adı >.**  
  
4.  Tam zamanında hata ayıklayıcı penceresinde, hata ayıklama için kullanmak istediğiniz Visual Studio sürümünü seçin.  
  
     ![JustInTimeDebugger](../debugger/media/justintimedebugger.png "JustInTimeDebugger")  
  
5.  Yeni bir örneğini Visual Studio başlatılır ve yürütme sırasında durduruldu `Debugger.Launch()` yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklayıcısı güvenliği](../debugger/debugger-security.md)   
 [Yönetilen Kodda Hata Ayıklama](../debugger/debugging-managed-code.md)