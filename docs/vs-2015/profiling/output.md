---
title: Çıkış | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 5e286e61-4548-42cf-a635-e608c5edbe2b
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 26a9532bcf0e641d9ad27522f207493b905dc471
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68179557"
---
# <a name="output"></a>Çıkış
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**Çıkış** seçeneği performans oturumu için profil oluşturma veri dosyasının adını belirtir. **Çıkış** ile birlikte kullanılmalıdır **Başlat** seçeneği.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
VSPerfCmd.exe /Start:Method /Output:FileName [Options]  
```  
  
#### <a name="parameters"></a>Parametreler  
 `FileName`  
 Veri dosyasının adı. Tam ve kısmi yollar kabul edilir. Bir yol belirtilmezse, dosyayı geçerli dizinde oluşturulur.  
  
## <a name="required-options"></a>Gerekli seçenekleri  
 **Çıkış** seçeneği kullanılmalıdır **Başlat** seçeneği.  
  
 **Başlat:** `Method`  
 Çıkış dosyası adını belirtir.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte, profil oluşturma veri dosyasını geçerli dizinde oluşturulur.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Oluşturma Hizmetleri](../profiling/command-line-profiling-of-services.md)
