---
title: Tam zamanında hata ayıklayıcı devre dışı bırakma | Microsoft Docs
ms.date: 05/23/2018
ms.topic: troubleshooting
helpviewer_keywords:
- debugging [Visual Studio], Just-In-Time
- Just-In-Time debugging
ms.assetid: 14972d5f-69bc-479b-9529-03b8787b118f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8c848281a89213a216bd8ec3ac1e651b6dfc32e4
ms.sourcegitcommit: 1c8e07b98fc0a44b5ab90bcef77d9fac7b3eb452
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/25/2019
ms.locfileid: "56796420"
---
# <a name="disable-the-just-in-time-debugger"></a>Anında Hata Ayıklayıcı’yı devre dışı bırakma

Tam zamanında hata ayıklayıcı iletişim kutusu içinde çalışan bir uygulamanın hata oluştuğunda açın ve uygulama devam etmesini engelleyebilir.

Tam zamanında hata ayıklayıcı, hata ayıklama için Visual Studio'yu başlatmak için seçeneği sunar. Olmalıdır [Visual Studio](http://visualstudio.microsoft.com) veya başka bir seçilen hata ayıklayıcı hata hakkında ayrıntılı bilgi görüntülemek veya hata ayıklarken için yüklü.

Visual Studio sürümünü kullanıyorsanız ve hata ayıklama için bkz. denemek istiyorsanız [tam zamanında hata ayıklayıcı ile hata ayıklama](../debugger/debug-using-the-just-in-time-debugger.md). Hatayı düzeltin veya tam zamanında hata ayıklayıcı açmasının tutmak istediğiniz olamaz varsa [Visual Studio'dan devre dışı bırakma, Just-ın-Time hata ayıklama](debug-using-the-just-in-time-debugger.md#BKMK_Enabling).

Visual Studio yüklü, ancak artık iş olsaydı gerekebilir [Windows kayıt defterinden devre dışı bırakma, Just-ın-Time hata ayıklama](debug-using-the-just-in-time-debugger.md#disable-just-in-time-debugging-from-the-windows-registry).

Visual Studio yüklü yoksa, tam zamanında hata ayıklamayı veya sunucu tarafı hata ayıklamasını devre dışı bırakarak hata ayıklamayı engelleyebilir.

- Bir web uygulamasını çalıştırmak çalışıyorsanız, komut dosyası hata ayıklaması devre dışı bırakın:

  Windows içinde **Denetim Masası** > **ağ ve Internet** > **Internet Seçenekleri**seçin **betik hata ayıklama (devre dışı bırak Internet Explorer)** ve **devre dışı bırak (diğer) ayıklamasını**. Uygulanacak adımlar ve ayarlarını Windows ve tarayıcınızı sürümünüze bağlıdır.

  ![JIT Internet Seçenekleri](../debugger/media/jitinternetoptions.png "JIT Internet Seçenekleri")

- IIS'de ASP.NET web uygulaması barındırıyorsanız, sunucu tarafı hata ayıklamasını devre dışı bırakın:

  1. IIS Yöneticisi'nde **özellikler görünümü**altında **ASP.NET** bölümünde, çift **.NET derleme**, veya seçin ve ardından **açık özellik**içinde **eylemleri** bölmesi.
  1. Altında **davranışı** > **hata ayıklama**seçin **False**. IIS eski sürümlerinde adımlar farklıdır.

Tam zamanında hata ayıklama devre dışı bıraktıktan sonra uygulamaya normal olarak çalışır ve hatayı işlemek mümkün olabilir.

Uygulamanın yine işlenmemiş bir hata varsa bir hata iletisini görebilirsiniz veya uygulama kilitlenme veya askıda olabilir. Uygulamayı, normalde hata düzeltilene kadar çalışmayacaktır. Uygulama sahibine başvurun ve sorunu gidermek için isteyin deneyebilirsiniz.
