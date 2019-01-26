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
ms.openlocfilehash: 23522f699d6fbb15e2f626e22e990163163eab5e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54940342"
---
# <a name="user-vsperfcmd"></a>Kullanıcı (VSPerfCmd)
**Kullanıcı** seçeneği profilli işlemin sahibi olan hesabının etki alanı ve kullanıcı adını belirtir. Bu seçenek, yalnızca oturum açan kullanıcının farklı bir kullanıcı olarak işlem çalışıyorsa gereklidir. İşlem sahibi kullanıcı adı sütununda listelenir **işlemleri** Windows Görev Yöneticisi'nin sekmesinde.  
  
 **Kullanıcı** seçeneği yalnızca de içeren bir komut satırında belirtilebilir **Başlat** seçeneği.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cmd  
VSPerfCmd.exe /Start:Method /Output:FileName /User:[Domain\]UserName [Options]  
```  
  
#### <a name="parameters"></a>Parametreler  
 `Domain`  
 Kullanıcının etki alanı adı.  
  
 `UserName`  
 Kullanıcı adı.  
  
## <a name="required-options"></a>Gerekli seçenekleri  
 **Kullanıcı** seçeneği yalnızca kullanılabilir ile **Başlat** seçeneği.  
  
 **Başlat:** `Method`  
 Belirtilen profil oluşturma metodu için profil oluşturucuyu başlatır.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, kullanımını gösterir **kullanıcı** seçeneği.  
  
```cmd  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /User:SYSTEM  
```  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil hizmetler](../profiling/command-line-profiling-of-services.md)