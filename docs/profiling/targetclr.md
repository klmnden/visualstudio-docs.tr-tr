---
title: TargetCLR | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: f9732480-287f-40f1-a4ff-b112e143b940
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ed0891715f6c9a0f4f89249a6ca5ac6415bad038
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53967128"
---
# <a name="targetclr"></a>TargetCLR
**TargetCLR** seçeneği bir uygulamada birden fazla CLR sürümü yüklendiğinde, ortak dil çalışma zamanı (CLR) sürümünü profiline belirtir.  
  
 Varsayılan olarak, [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma araçları hedef uygulama tarafından yüklenen CLR ilk sürümü.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cmd  
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
  
```cmd  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe /TargetCLR:v4.0.11003  
```