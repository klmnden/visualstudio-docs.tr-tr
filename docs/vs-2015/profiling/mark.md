---
title: İşareti | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 1d72cef3-bb09-4bbb-8864-6ea0ab623ff9
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4d1bd78f356ed8fc48db9b7712e46fe88e8d3a83
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49297576"
---
# <a name="mark"></a>İşaret
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

VSPerfCmd.exe **işareti** seçeneği, profil oluşturma veri dosyası içinde belirtilen bilgileri ekler. Mark, profil oluşturucunun UI işareti rapor görünümü veya ayrı bir VSPerfReport raporlarında listelenebilir. **İşareti** başlangıç ve bitiş noktalarını rapor ve görünümü filtreleri belirtmek için kullanılabilir.  
  
 **İşareti** seçeneği, komut satırında belirtilen tek seçenek olması gerekir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
VSPerfCmd.exe /Mark:MarkID,[MarkName]  
```  
  
#### <a name="parameters"></a>Parametreler  
 `MarkID`  
 Profil Oluşturucu görünümleri ve raporları işaret kimliği olarak listelenen bir kullanıcı tanımlı bir tamsayı. `MarkID` benzersiz olması gerekmez.  
  
 `MarkName`  
 (İsteğe bağlı) Profil Oluşturucu görünümleri ve raporları işareti adı olarak listelenen bir kullanıcı tanımlı bir dize. Varsa `MarkName` belirtilmezse, işareti listenin işareti adı alanı boş değil. Boşluk veya tırnak işaretleri ("/") eğik iletme dizeleri alın.  
  
## <a name="example"></a>Örnek  
 Bu örnek, işareti 123 kimliği ve "TestMark" işareti adını ekler.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe  
VSPerfCmd.exe /Mark:123,TestMark  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Oluşturma Hizmetleri](../profiling/command-line-profiling-of-services.md)



