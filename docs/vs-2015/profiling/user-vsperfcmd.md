---
title: Kullanıcı (VSPerfCmd) | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: ee1a478e-374d-4f30-ae28-d260b9d4723a
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b390852c94477a6b02d43b0dbc7678384c622ced
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49302009"
---
# <a name="user-vsperfcmd"></a>Kullanıcı (VSPerfCmd)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**Kullanıcı** seçeneği profilli işlemin sahibi olan hesabının etki alanı ve kullanıcı adını belirtir. Bu seçenek, yalnızca oturum açan kullanıcının farklı bir kullanıcı olarak işlem çalışıyorsa gereklidir. İşlem sahibi, Windows Görev Yöneticisi'nin İşlemler sekmesinde kullanıcı adı sütununda listelenir.  
  
 **Kullanıcı** seçeneği yalnızca de içeren bir komut satırında belirtilebilir **Başlat** seçeneğini seçenek.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
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
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /User:SYSTEM  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Oluşturma Hizmetleri](../profiling/command-line-profiling-of-services.md)



