---
title: Önceki .NET Framework sürümlerini hedefF#
description: Kullanırken, .NET Framework'ün daha eski bir sürümü hedefleme hakkında bilgi edinin F# Visual Studio'da.
ms.date: 07/11/2018
ms.topic: troubleshooting
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
monikerRange: vs-2017
ms.openlocfilehash: 2e0d580ac18142010a306d3fb4de19eb69b0b91b
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66746708"
---
# <a name="target-older-versions-of-net-f"></a>Eski .NET sürümlerini hedefleyen (F#)

.NET Framework 2.0, 3.0 veya 3.5 hedeflemek denerseniz aşağıdaki hata görünebilir bir F# proje Windows 8.1 Visual Studio yüklü olduğunda:

**Bu proje 2.0 gerektirir F# çalışma zamanı, ancak bu çalışma zamanı yüklü değil.**

Bu hata koşulları altında aşağıdaki birleşimi bilinmektedir:

- Windows 8.1 Visual Studio yüklenmiş.

- Visual Studio yüklemeden önce .NET Framework 3.5 etkinleştirme kaydetmedi.

- Projeniz .NET Framework 2.0, 3.0 veya 3.5 hedefler.

Visual Studio yükleme sırasında .NET Framework'ün yüklü sürümlerini algılar. Visual Studio'yu yükler F# yalnızca .NET Framework 3.5 yüklü etkin ve 2.0 çalışma zamanı.

## <a name="resolve-the-error"></a>Hatayı çözün

Bu hatayı gidermek için şunlardan birini yapabilirsiniz:

- Hedef .NET Framework'ün daha yeni bir sürümü.

- Windows 8.1 üzerinde .NET Framework 3.5 etkinleştirme ve yüklemeyi F# Visual Studio onarmayı tarafından 2.0 çalışma zamanı. Bunu yapmak için adımları izleyin.

### <a name="to-enable-the-net-framework-35-on-windows-81"></a>Windows 8.1 üzerinde .NET Framework 3.5 etkinleştirmek için

1. Üzerinde **Başlat** ekranında, yazın **Denetim Masası**.

   Siz yazarken **Denetim Masası** simgesi görünür altında **uygulamaları** başlığı.

2. Seçin **Denetim Masası** simgesini seçin **programlar** simgesini seçip **kapatma Windows özelliklerini aç veya Kapat** bağlantı.

3. Emin olun **.NET Framework 3.5 (.NET 2.0 ve 3.0 içerir)** onay kutusunun seçili olduğundan ve ardından **Tamam** düğmesi. .NET Framework'ün isteğe bağlı bileşenler için herhangi bir alt düğüm için onay kutularını işaretleyin gerek yoktur.

   Zaten yapmadıysanız, .NET Framework 3.5 etkinleştirilir.

### <a name="to-install-the-f-20-runtime"></a>Yüklenecek F# 2.0 çalışma zamanı

İzleyin [Visual Studio'yu onarmak için adımları](../install/repair-visual-studio.md).

## <a name="see-also"></a>Ayrıca bkz.

- [F#Kılavuzu (.NET Framework)](/dotnet/fsharp/)
- [F#Visual Studio'da](fsharp-visual-studio.md)