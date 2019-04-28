---
title: İşareti | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 1d72cef3-bb09-4bbb-8864-6ea0ab623ff9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 440401f8c46a3920fce6c8e0d29f630a24103f65
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62999991"
---
# <a name="mark"></a>İşaret
*VSPerfCmd.exe* **işareti** seçeneği, profil oluşturma veri dosyası içinde belirtilen bilgileri ekler. Mark, profil oluşturucunun UI işareti rapor görünümü veya ayrı bir VSPerfReport raporlarında listelenebilir. **İşareti** başlangıç ve bitiş noktalarını rapor ve görünümü filtreleri belirtmek için kullanılabilir.

 **İşareti** seçeneği, komut satırında belirtilen tek seçenek olması gerekir.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Mark:MarkID,[MarkName]
```

#### <a name="parameters"></a>Parametreler
 `MarkID` Profil Oluşturucu görünümleri ve raporları işaret kimliği olarak listelenen bir kullanıcı tanımlı bir tamsayı. `MarkID` benzersiz olması gerekmez.

 `MarkName` (İsteğe bağlı) Profil Oluşturucu görünümleri ve raporları işareti adı olarak listelenen bir kullanıcı tanımlı bir dize. Varsa `MarkName` belirtilmezse, işareti listenin işareti adı alanı boş değil. Boşluk veya tırnak işaretleri ("/") eğik iletme dizeleri alın.

## <a name="example"></a>Örnek
 Bu örnek, işareti 123 kimliği ve "TestMark" işareti adını ekler.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp
VSPerfCmd.exe /Launch:TestApp.exe
VSPerfCmd.exe /Mark:123,TestMark
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)