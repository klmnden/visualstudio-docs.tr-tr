---
title: CrossSession | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: b9fcb9c3-7903-478c-9b7c-dbd94092fcba
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8087f620f457f1e88ee6dc9ffff90f5c8747e50d
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56626836"
---
# <a name="crosssession"></a>CrossSession
*VSPerfCmd.exe* **CrossSession** seçeneği herhangi bir konsol oturumundan verileri toplamak profil oluşturucu sağlar. **CrossSession** seçeneği kullanılmalıdır **Başlat** seçeneği.

 Kısaltması kullanabileceğiniz **CS** yerine **CrossSession**.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Start:Method /CrossSession [Options]
```

#### <a name="parameters"></a>Parametreler
 Hiçbiri

## <a name="valid-options"></a>Geçerli seçenekler şunlardır:
 Başka bir oturumda oluşturmayı etkinleştirmek için **CrossSession** seçeneği belirtilmelidir **Başlat** seçeneği. **CrossSession** de birinde belirtilmelidir sonraki **VSPerfCmd ekleme** ve **ayırma** komutları.

 **Başlat:** `Method` **Başlat** seçeneği belirtilen profil oluşturma metodu için profil oluşturucuyu başlatır.

 **Ekleme:** _PID_[**,**_PID_] belirtilen işlemler için profil oluşturma başlar.

 **Ayırma**[**:**_PID_[,_PID_]] belirtilen işlemler profil oluşturmayı durdurur.

## <a name="example"></a>Örnek
 Bu örnekte, **CrossSession** seçeneği, başka bir konsol oturumu başlatılmasından bir uygulamaya eklemek için kullanılır.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /CrossSession
VSPerfCmd.exe /Attach:12345 /CS
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)