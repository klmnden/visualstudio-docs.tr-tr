---
title: Waıtstart | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 6c737177-2dfb-4150-963e-a49ac9aaa591
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6307dcad45b7e2c8164aa892c4598d577e4ea464
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56614642"
---
# <a name="waitstart"></a>WaitStart
Waıtstart seçeneği nedenlerini *VSPerfCmd.exe* yalnızca profil oluşturucu başlatıldı veya belirtilen sayıda saniye geçtikten döndürmek için başlangıç alt komutu. Varsayılan olarak, başlangıç komut hemen döndürür. Başlangıç alt komutu, profil oluşturucu başlatma olmadan döndürürse, hata döndürülür. Saniye sayısı belirtilmezse, Start komutunu süresiz olarak bekler.

 Bu profil oluşturucu başlatıldı sağlamak üzere toplu iş dosyalarında Waıtstart seçeneği kullanışlıdır.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Start:Method /Output:FileName[Options] /StartWait[:Seconds]
```

#### <a name="parameters"></a>Parametreler
 `Seconds` Başlangıç alt komuttan dönmeden önce beklenecek saniye sayısı.

## <a name="required-options"></a>Gerekli seçenekleri
 Waıtstart seçeneği yalnızca başlangıç alt komut ile kullanılabilir.

 **Çıkış:** `filename` Çıkış dosyası adını belirtir.

## <a name="remarks"></a>Açıklamalar

## <a name="example"></a>Örnek
 Bu toplu dosya örnekte Start komutunu profil oluşturucuyu başlatmak 5 saniye bekler.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /WaitStart:5
if not %errorlevel% 0 goto :error_tag
VSPerfCmd.exe /Launch:TestApp.exe
goto :end
:error_tag
@echo Could not start Profiler!
@echo Error %errorlevel%
:end
```