---
title: Derleme Öncesi Olay-Derleme Sonrası Olay Komut Satırı İletişim Kutusu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6fa3ec42d90611c4618b786c0263ed0732dca093
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55023294"
---
# <a name="pre-build-eventpost-build-event-command-line-dialog-box"></a>Derleme Öncesi Olay/Derleme Sonrası Olay Komut Satırı İletişim Kutusu
Ön veya derleme sonrası olay için yazdığınız [derleme olayları sayfası, Proje Tasarımcısı (C#)](../../ide/reference/build-events-page-project-designer-csharp.md) Düzenle doğrudan kutusu veya öncesi ve sonrası derleme makroları kullanılabilir makroların bir listeden seçebilirsiniz.

> [!NOTE]
> Derleme öncesi olayları, projenin güncel olduğundan ve hiçbir derlemenin tetiklenmesinin çalıştırmayın.


## <a name="ui-element-list"></a>UI öğe listesi
 **Komut satırı düzenleme kutusu**

 Derleme öncesi veya derleme sonrası için çalıştırılacak etkinlik içermiyor.

> [!NOTE]
> Ekleme bir `call` .bat dosyaları çalıştıran tüm derleme sonrası komutları önce deyimi. Örneğin, `call C:\MyFile.bat` veya `call C:\MyFile.bat call C:\MyFile2.bat`.


 **Makroları**

 Makro komut satırı düzenleme kutusuna eklenecek bir listesini görüntülemek için düzenleme kutusunu genişletir.

 **Makro tablosu**

 Uygun makroları ve değerini listeler. Aşağıdaki makroları, her bir açıklaması için bkz. Komut satırı düzenleme kutusuna eklenecek bir anda yalnızca bir makro seçebilirsiniz.

 **Ekle**

 Komut satırı ekler düzenleme kutusu makrosu tablodan seçilen makrosu.

### <a name="macros"></a>Makrolar
 Dosya konumlarını belirtin ya da birden çok seçimin söz konusu olduğunda giriş dosyası gerçek adını almak için bu makrolar dilediğinizi kullanabilirsiniz. Bu makrolar, büyük küçük harfe duyarlı değildir.

|Makrosu|Açıklama|
|-----------|-----------------|
|`$(ConfigurationName)`|Geçerli proje yapılandırması, örneğin "Debug" adı.|
|`$(OutDir)`|Çıkış dosyası dizinine, proje dizinine göreli yolu. Bu çıktı dizini özelliğinin değerini çözümler. Sondaki ters eğik çizgi içerir '\\'.|
|`$(DevEnvDir)`|(Sürücü ve yol ile tanımlanır); Visual Studio yükleme dizini sondaki ters eğik çizgi içerir '\\'.|
|`$(PlatformName)`|Şu anda hedeflenen platformun adı. Örneğin, "AnyCPU".|
|`$(ProjectDir)`|(Sürücü ve yol ile tanımlanır); proje dizini sondaki ters eğik çizgi içerir '\\'.|
|`$(ProjectPath)`|(Sürücü, yol, temel adı ve dosya uzantısı ile tanımlanır) projenin mutlak yol adı.|
|`$(ProjectName)`|Temel projenin adı.|
|`$(ProjectFileName)`|(Temel adı ve dosya uzantısı ile tanımlanır) proje dosya adı.|
|`$(ProjectExt)`|Projenin dosya uzantısı. İçerdiğinden '.' dosya uzantısı önce.|
|`$(SolutionDir)`|(Sürücü ve yol ile tanımlanır); çözüm dizini sondaki ters eğik çizgi içerir '\\'.|
|`$(SolutionPath)`|(Sürücü, yol, temel adı ve dosya uzantısı ile tanımlanır) çözümü mutlak yol adı.|
|`$(SolutionName)`|Çözümün temel adı.|
|`$(SolutionFileName)`|(Temel adı ve dosya uzantısı ile tanımlanır) çözüm dosyasının adı.|
|`$(SolutionExt)`|Çözüm öğesinin dosya uzantısı. İçerdiğinden '.' dosya uzantısı önce.|
|`$(TargetDir)`|Derleme (sürücü ve yol ile tanımlanır) için birincil çıkış dosyasının dizin. Sondaki ters eğik çizgi içerir '\\'.|
|`$(TargetPath)`|Mutlak yol (sürücü, yol, temel adı ve dosya uzantısı ile tanımlanır) yapı için birincil çıkış dosyasının adı.|
|`$(TargetName)`|Derleme için birincil çıkış dosyasının temel adı.|
|`$(TargetFileName)`|Derleme (temel adı ve dosya uzantısı olarak tanımlanır) için birincil çıkış dosyasının dosya adı.|
|`$(TargetExt)`|Derleme için birincil çıkış dosyasının dosya uzantısı. İçerdiğinden '.' dosya uzantısı önce.|

## <a name="see-also"></a>Ayrıca Bkz.

- [Visual Studio'da Özel Derleme Olayları Belirtme](../../ide/specifying-custom-build-events-in-visual-studio.md)
- [Derleme Olayları Sayfası, Proje Tasarımcısı (C#)](../../ide/reference/build-events-page-project-designer-csharp.md)
- [Nasıl yapılır: Derleme olayları belirtme (Visual Basic)](../../ide/how-to-specify-build-events-visual-basic.md)
- [Nasıl yapılır: Derleme olayları belirtme (C#)](../../ide/how-to-specify-build-events-csharp.md)