---
title: Genel proje özellikleri (Android C++) | Microsoft Docs
ms.custom: ''
ms.date: 10/23/2017
ms.technology: vs-ide-mobile
ms.topic: conceptual
ms.assetid: 65f4868b-b864-4989-a275-1e51869ef599
author: corob
ms.author: mblome
manager: jillfra
f1_keywords:
- VC.Project.VCConfiguration.OutputDirectory
- VC.Project.VCConfiguration.IntermediateDirectory
- VC.Project.VCConfiguration.TargetName
- VC.Project.VCConfiguration.TargetExt
- VC.Project.VCConfiguration.DeleteExtensionsOnClean
- VC.Project.VCConfiguration.BuildLogFile
- VC.Project.VCConfiguration.PlatformToolset
- VC.Project.VCConfiguration.ConfigurationType
- VC.Project.VCConfiguration.DeleteExtensionsOnClean
- VC.Project.VCConfiguration.UseOfSTL
- VC.Project.VCConfiguration.ThumbMode
ms.workload:
- xplat-cplusplus
ms.openlocfilehash: 4bb6f26fe40b639b43cb803577a785fa9b48823d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62818953"
---
# <a name="general-project-properties-android-c"></a>Genel Proje Özellikleri (Android C++)

Özellik | Açıklama | Seçenekleri
--- | ---| ---
Çıkış dizini | Çıkış dosyası dizinine göreli bir yol belirtir; ortam değişkenleri içerebilir.
Ara dizin | Ara dosya dizinine göreli bir yol belirtir; ortam değişkenleri içerebilir.
Hedef Adı | Bu projenin oluşturacağı bir dosya adını belirtir.
Hedef uzantısı | Bu projenin oluşturacağı dosya uzantısını belirtir. (Örnek: *.exe* veya *.dll*)
Temizlemede silinecek uzantılar | Joker karakter belirtimi Ara dizindeki, Temizlemede silin veya yeniden dosyalar için noktalı virgülle ayrılmış listesidir.
Derleme günlüğü dosyası | Günlük kaydı ne zaman oluşturulacağını yazılacak derleme günlüğü dosyasını belirtir.
Platform araç takımı | Geçerli yapılandırmayı oluşturmak için kullanılan araç kümesini belirtir. Aksi halde, varsayılan araç kümesi kullanılır
Yapılandırma türü | Bu yapılandırmanın oluşturduğu çıkışın türünü belirtir. | **Dinamik kitaplık (.so)** -dinamik kitaplık (*.so*)<br>**Statik kitaplık (.a)** -statik kitaplık (*.a*)<br>**Yardımcı program** - yardımcı programı<br>**Derleme görevleri dosyası** -derleme görevleri dosyası<br>
Hedef API düzeyi | Android NDK API düzeyi bu yapılandırmanın hedeflediği.
STL kullanımı | Bu yapılandırma için kullanmak için hangi C++ Standart Kitaplığı belirtir. | **En düşük C++ çalışma zamanı kitaplığı (system)**<br>**C++çalışma zamanı statik kitaplığı (gabi ++ _static)**<br>**C++çalışma zamanı paylaşılan kitaplığı (gabi ++ _shared)**<br>**STLport çalışma zamanı statik kitaplığı (stlport_static)**<br>**STLport çalışma zamanı paylaşılan kitaplığı (stlport_shared)**<br>**GNU STL statik kitaplığı (gnustl_static)**<br>**GNU STL paylaşılan kitaplığı (gnustl_shared)**<br>**LLVM libc ++ statik kitaplığı (c ++ _static)**<br>**LLVM libc ++ paylaşılan kitaplığı (c ++ _shared)**<br>
Thumb modu | Thumb mikro mimarisi için yürütülen kodu oluşturur. Bu, yalnızca arm mimarisi için geçerlidir. | **Thumb**<br>**ARM**<br>**Devre dışı**<br>
