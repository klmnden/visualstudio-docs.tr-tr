---
title: TargetCLR | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: f9732480-287f-40f1-a4ff-b112e143b940
caps.latest.revision: 16
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 1e4ca52f631b3e2de9c01daab7e6268c42f20268
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54801202"
---
# <a name="targetclr"></a>TargetCLR
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**TargetCLR** seçeneği bir uygulamada birden fazla CLR sürümü yüklendiğinde, ortak dil çalışma zamanı (CLR) sürümünü profiline belirtir.  
  
 Varsayılan olarak, [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] profil oluşturma araçları hedef uygulama tarafından yüklenen CLR ilk sürümü.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
VSPerfCmd.exe {/Launch:AppName | /Attach:PID} /TargetCLR[:ClrVersion] [Options]   
```  
  
#### <a name="parameters"></a>Parametreler  
 `ClrVersion`  
 CLR sürüm numarası. Sürüm biçimi **vN.N.NNNNN**.  
  
## <a name="required-options"></a>Gerekli seçenekleri  
 **TargetCLR** seçeneği yalnızca kullanılabilir ile **başlatma** veya **iliştirme** seçenekleri.  
  
 **Başlat:** `AppName`  
 Belirtilen uygulamayı başlatır ve profile başlatır.  
  
 **Ekleme:** `PID`  
 Belirtilen işlem profili başlar.  
  
## <a name="example"></a>Örnek  
 Bu örnekte, TargetCLR seçeneği, CLR sürümü 4.0.11003 profili emin emin olmak için kullanılır.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe /TargetCLR:v4.0.11003  
```
