---
title: TargetCLR | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: f9732480-287f-40f1-a4ff-b112e143b940
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 479f7e1cbd85c0421497020ae1fc108154ca639a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62968320"
---
# <a name="targetclr"></a>TargetCLR
**TargetCLR** seçeneği bir uygulamada birden fazla CLR sürümü yüklendiğinde, ortak dil çalışma zamanı (CLR) sürümünü profiline belirtir.

 Varsayılan olarak, [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] profil oluşturma araçları hedef uygulama tarafından yüklenen CLR ilk sürümü.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe {/Launch:AppName | /Attach:PID} /TargetCLR[:ClrVersion] [Options]
```

#### <a name="parameters"></a>Parametreler
 `ClrVersion` CLR sürüm numarası. Sürüm biçimi **vN.N.NNNNN**.

## <a name="required-options"></a>Gerekli seçenekleri
 **TargetCLR** seçeneği yalnızca kullanılabilir ile **başlatma** veya **iliştirme** seçenekleri.

 **Başlat:** `AppName` Belirtilen uygulamayı başlatır ve profile başlatır.

 **Ekleme:** `PID` Belirtilen işlem profili başlar.

## <a name="example"></a>Örnek
 Bu örnekte, TargetCLR seçeneği, CLR sürümü 4.0.11003 profili emin emin olmak için kullanılır.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp
VSPerfCmd.exe /Launch:TestApp.exe /TargetCLR:v4.0.11003
```