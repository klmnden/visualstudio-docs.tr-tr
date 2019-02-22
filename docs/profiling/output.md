---
title: Çıkış | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 5e286e61-4548-42cf-a635-e608c5edbe2b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 78d5b39908bc0ffa39533c22ea4effcbe97397b7
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56613810"
---
# <a name="output"></a>Çıkış
**Çıkış** seçeneği performans oturumu için profil oluşturma veri dosyasının adını belirtir. **Çıkış** ile birlikte kullanılmalıdır **Başlat** seçeneği.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Start:Method /Output:FileName [Options]
```

#### <a name="parameters"></a>Parametreler
 `FileName` Veri dosyasının adı. Tam ve kısmi yollar kabul edilir. Bir yol belirtilmezse, dosyayı geçerli dizinde oluşturulur.

## <a name="required-options"></a>Gerekli seçenekleri
 **Çıkış** seçeneği kullanılmalıdır **Başlat** seçeneği.

 **Başlat:** `Method` Çıkış dosyası adını belirtir.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte, profil oluşturma veri dosyasını geçerli dizinde oluşturulur.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)