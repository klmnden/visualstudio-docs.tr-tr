---
title: Kullanıcı (VSPerfCmd) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: ee1a478e-374d-4f30-ae28-d260b9d4723a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7039422a6934eb4dfa007d216fdc0a70e0da32e9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62830843"
---
# <a name="user-vsperfcmd"></a>Kullanıcı (VSPerfCmd)
**Kullanıcı** seçeneği profilli işlemin sahibi olan hesabının etki alanı ve kullanıcı adını belirtir. Bu seçenek, yalnızca oturum açan kullanıcının farklı bir kullanıcı olarak işlem çalışıyorsa gereklidir. İşlem sahibi kullanıcı adı sütununda listelenir **işlemleri** Windows Görev Yöneticisi'nin sekmesinde.

 **Kullanıcı** seçeneği yalnızca de içeren bir komut satırında belirtilebilir **Başlat** seçeneği.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Start:Method /Output:FileName /User:[Domain\]UserName [Options]
```

#### <a name="parameters"></a>Parametreler
 `Domain` Kullanıcının etki alanı adı.

 `UserName` Kullanıcı adı.

## <a name="required-options"></a>Gerekli seçenekleri
 **Kullanıcı** seçeneği yalnızca kullanılabilir ile **Başlat** seçeneği.

 **Başlat:** `Method` Belirtilen profil oluşturma metodu için profil oluşturucuyu başlatır.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, kullanımını gösterir **kullanıcı** seçeneği.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /User:SYSTEM
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)