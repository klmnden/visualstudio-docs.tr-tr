---
title: 'Hata: ASP.NET yüklü değil | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.http_not_supported
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Web applications, errors
- debugger, Web application errors
- error messages, ASP.NET
- ASP.NET, installation error messages
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- aspnet
ms.openlocfilehash: 09c10019f4a3efd369398964eb1cf957968b4d10
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54976504"
---
# <a name="error-aspnet-not-installed"></a>Hata: ASP.NET yüklü değil
Bu hata oluştuğunda, [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] doğru hata ayıklamaya çalıştığınız bilgisayarda yüklü değil. Bu gelebilir [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] hiç yüklenmemiş ya da [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] ilk yüklenen ve IIS daha sonra yüklendi.  
  
### <a name="to-reinstall-aspnet"></a>ASP.NET yeniden yüklemek için  
  
1. Bir komut istemi penceresinden aşağıdaki komutu çalıştırın:  
  
   ```cmd
   \WINDOWS\Microsoft.NET\Framework\version\aspnet_regiis -i  
   ```  
  
    Burada *sürüm* v1.0.370 gibi bilgisayarınızda yüklü .NET Framework sürüm numarasını temsil eder. Framework sürümü bakarak belirleyebilirsiniz `\WINDOWS\Microsoft.NET\Framework` dizin.  
  
   > [!NOTE]
   >  Windows Server 2003 ile yükleyebileceğiniz [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] kullanarak **Program Ekle veya Kaldır** Denetim Masası'nda.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Web Uygulamalarında Hata Ayıklama: Hatalar ve Sorun Giderme](../debugger/debugging-web-applications-errors-and-troubleshooting.md)
