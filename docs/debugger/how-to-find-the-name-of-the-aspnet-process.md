---
title: ASP.NET çalışan işlemine bulun | Microsoft Docs
ms.date: 11/04/2018
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- ASP.NET debugging, ASP.NET process
- ASP.NET process
ms.assetid: 931a7597-b0f0-4a28-931d-46e63344435f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- aspnet
ms.openlocfilehash: 27221a4ae47b9fb06130b550ceb6d3cc1f00dce0
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56680964"
---
# <a name="find-the-name-of-the-aspnet-process"></a>ASP.NET işleminin adını bulma

Çalışan bir hata ayıklamak için [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] uygulama, Visual Studio hata ayıklayıcısını İliştir gerekir için [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] ada göre işleyin.

**Bir ASP.NET uygulaması çalışan işlemi bulmak için:**

1. Birlikte çalıştığından, Visual Studio'da Uygulama'yı **hata ayıklama** > **iliştirme**.

1. İçinde **iliştirme** iletişim kutusunda, türü işleminin ilk harflerini adları aşağıdaki listeden veya arama kutusuna girin. Çalıştıran bir ASP.NET uygulaması çalıştıran bir bilgisayardır. Uygulamanın hatalarını ayıklamak için bu işleme.

    - *W3wp.exe* IIS 6.0 ve üzeri olan.
    - *aspnet_wp.exe* IIS'in önceki sürümlerinde olduğu.
    - *iisexpress.exe* Iısexpress olduğu.
    - *DotNet.exe* ASP.NET Core.
    - *inetinfo.exe* işlemde çalışan daha eski bir ASP uygulama.

>[!NOTE]
>Visual Studio 2012 ve önceki [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] kod dosya sisteminde ve test sunucuda çalıştırılan *WebDev.WebServer.exe* veya *WebDev.WebServer40.exe*. Bu durumda, için yerel hata ayıklama için bağlayabilmenizi *WebDev.WebServer.exe* veya *WebDev.WebServer40.exe* yerine [!INCLUDE[vstecasp](../code-quality/includes/vstecasp_md.md)] işlem.

**Ayrıca bkz:**

- [Çalışan bir işleme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md)
- [Uzaktan hata ayıklama web uygulamaları için Önkoşullar](/visualstudio/debugger/remote-debugging-aspnet-on-a-remote-iis-7-5-computer)
- [Sistem gereksinimleri](../debugger/aspnet-debugging-system-requirements.md)
- [ASP.NET uygulamalarında hata ayıklama](../debugger/how-to-enable-debugging-for-aspnet-applications.md)