---
title: Derleme Öncesi Olay-Derleme Sonrası Olay Komut Satırı İletişim Kutusu
ms.date: 11/04/2016
ms.technology: vs-ide-compile
ms.topic: reference
f1_keywords:
- cs.ProjectPropertiesBuildEventsBuilder
- vb.ProjectPropertiesBuildEventsBuilder
helpviewer_keywords:
- $(SolutionExt)
- $(ProjectDir)
- $(TargetPath)
- $(ProjectExt)
- $(TargetFileName)
- $(PlatformName)
- $(SolutionName)
- macros, build events
- $(SolutionPath)
- $(ProjectPath)
- $(ProjectFileName)
- $(DevEnvDir)
- $(TargetName)
- $(TargetDir)
- $(SolutionDir)
- $(TargetExt)
- $(OutDir)
- $(ConfigurationName)
- $(SolutionFileName)
- $(ProjectName)
- build events, macros
ms.assetid: d49b2c57-24bf-4fb2-8351-5c4b6cca938f
author: ghogen
ms.author: ghogen
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d5671a75a847d81caedeffc17ea436eade060f3e
ms.sourcegitcommit: 85d66dc9fea3fa49018263064876b15aeb6f9584
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/24/2019
ms.locfileid: "68461315"
---
# <a name="pre-build-eventpost-build-event-command-line-dialog-box"></a>Oluşturma öncesi olay/oluşturma sonrası olay komut satırı iletişim kutusu

[Derleme olayları sayfası, proje TasarımcısıC#()](../../ide/reference/build-events-page-project-designer-csharp.md) için doğrudan düzenleme kutusuna derleme öncesi veya sonrası olay yazabilir veya kullanılabilir makrolar listesinden ön ve derleme sonrası makrolar seçebilirsiniz.

> [!NOTE]
> Proje güncel değilse ve derleme tetikleniyorsa, ön derleme olayları çalışmaz.

## <a name="ui-element-list"></a>UI öğe listesi

**Komut satırı düzenleme kutusu**

Oluşturma öncesi ya da derleme sonrası için çalıştırılacak olayları içerir.

> [!NOTE]
> . Bat `call` dosyalarını çalıştıran tüm derleme sonrası komutlarının önüne bir ifade ekleyin. Örneğin, `call C:\MyFile.bat` veya `call C:\MyFile.bat call C:\MyFile2.bat`.

**Larının**

Komut satırı düzenleme kutusuna eklenecek makroların listesini göstermek için düzenleme kutusunu genişletir.

**Makro tablosu**

Kullanılabilir makroları ve değerini listeler. Her birinin açıklaması için aşağıdaki makroları inceleyin. Komut satırı düzenleme kutusuna eklemek için tek seferde yalnızca bir makro seçebilirsiniz.

**Ekle**

Makro tablosunda seçilen makro komut satırı düzenleme kutusuna ekler.

### <a name="macros"></a>Makrolar

Bu makroların herhangi birini dosya konumları belirtmek için veya birden çok seçim durumunda giriş dosyasının gerçek adını almak için kullanabilirsiniz. Bu makrolar büyük/küçük harfe duyarlı değildir.

|Makrosu|Açıklama|
|-----------|-----------------|
|`$(ConfigurationName)`|Geçerli proje yapılandırmasının adı, örneğin "Debug".|
|`$(OutDir)`|Proje dizinine göre çıkış dosyası dizininin yolu. Bu, çıkış dizini özelliğinin değerini çözümler. '\\' Sonunda ters eğik çizgi içeriyor.|
|`$(DevEnvDir)`|Visual Studio yükleme dizini (sürücü ve yol ile tanımlanır); '\\' sonunda ters eğik çizgi içerir.|
|`$(PlatformName)`|Şu anda hedeflenen platformun adı. Örneğin, "AnyCPU".|
|`$(ProjectDir)`|Projenin dizini (sürücü ve yol ile tanımlanır); '\\' sonunda ters eğik çizgi içerir.|
|`$(ProjectPath)`|Projenin mutlak yol adı (sürücü, yol, taban adı ve dosya uzantısıyla tanımlanır).|
|`$(ProjectName)`|Projenin temel adı.|
|`$(ProjectFileName)`|Projenin dosya adı (taban adı ve dosya uzantısıyla tanımlanır).|
|`$(ProjectExt)`|Projenin dosya uzantısı. Dosya uzantısından önce '. ' içerir.|
|`$(SolutionDir)`|Çözümün dizini (sürücü ve yol ile tanımlanır); '\\' sonunda ters eğik çizgi içerir.|
|`$(SolutionPath)`|Çözümün mutlak yol adı (sürücü, yol, taban adı ve dosya uzantısıyla tanımlanır).|
|`$(SolutionName)`|Çözümün temel adı.|
|`$(SolutionFileName)`|Çözümün dosya adı (taban adı ve dosya uzantısıyla tanımlanır).|
|`$(SolutionExt)`|Çözümün dosya uzantısı. Dosya uzantısından önce '. ' içerir.|
|`$(TargetDir)`|Derleme için birincil çıkış dosyasının dizini (sürücü ve yol ile tanımlanır). '\\' Sonunda ters eğik çizgi içeriyor.|
|`$(TargetPath)`|Derleme için birincil çıkış dosyasının mutlak yol adı (sürücü, yol, taban adı ve dosya uzantısıyla tanımlanır).|
|`$(TargetName)`|Derleme için birincil çıkış dosyasının temel adı.|
|`$(TargetFileName)`|Derleme için birincil çıkış dosyasının dosya adı (temel ad ve dosya uzantısı olarak tanımlanır).|
|`$(TargetExt)`|Derleme için birincil çıkış dosyasının dosya uzantısı. Dosya uzantısından önce '. ' içerir.|

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da Özel Derleme Olayları Belirtme](../../ide/specifying-custom-build-events-in-visual-studio.md)
- [Derleme Olayları Sayfası, Proje Tasarımcısı (C#)](../../ide/reference/build-events-page-project-designer-csharp.md)
- [Nasıl yapılır: Derleme Olayları Belirtme (Visual Basic)](../../ide/how-to-specify-build-events-visual-basic.md)
- [Nasıl yapılır: Derleme Olayları Belirtme (C#)](../../ide/how-to-specify-build-events-csharp.md)