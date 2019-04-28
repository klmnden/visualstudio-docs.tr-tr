---
title: CrossSession | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: b9fcb9c3-7903-478c-9b7c-dbd94092fcba
caps.latest.revision: 15
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 05e1f2360b3257e44fde1af8be3554dd7fd95115
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62537191"
---
# <a name="crosssession"></a>CrossSession
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

VSPerfCmd.exe **CrossSession** seçeneği herhangi bir konsol oturumundan verileri toplamak profil oluşturucu sağlar. **CrossSession** seçeneği kullanılmalıdır **Başlat** seçeneği.  
  
 Kısaltması kullanabileceğiniz **CS** yerine **CrossSession**.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
VSPerfCmd.exe /Start:Method /CrossSession [Options]  
```  
  
#### <a name="parameters"></a>Parametreler  
 None  
  
## <a name="valid-options"></a>Geçerli seçenekler şunlardır:  
 Başka bir oturumda oluşturmayı etkinleştirmek için **CrossSession** seçeneği belirtilmelidir **Başlat** seçeneği. **CrossSession** de birinde belirtilmelidir sonraki **VSPerfCmd ekleme** ve **ayırma** komutları.  
  
 **Başlat:** `Method`  
 **Başlat** seçeneği belirtilen profil oluşturma metodu için profil oluşturucuyu başlatır.  
  
 **Ekleme:** _PID_[**,**_PID_]  
 Belirtilen işlemler için profil oluşturma başlar.  
  
 **Ayırma**[**:**_PID_[,_PID_]]  
 Belirtilen işlemler profil oluşturmayı durdurur.  
  
## <a name="example"></a>Örnek  
 Bu örnekte, **CrossSession** seçeneği, başka bir konsol oturumu başlatılmasından bir uygulamaya eklemek için kullanılır.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /CrossSession  
VSPerfCmd.exe /Attach:12345 /CS  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Oluşturma Hizmetleri](../profiling/command-line-profiling-of-services.md)
