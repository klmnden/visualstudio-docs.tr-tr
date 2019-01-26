---
title: VSIX v3'te Ngen desteği | Microsoft Docs
ms.date: 11/09/2016
ms.topic: conceptual
ms.assetid: 1472e884-c74e-4c23-9d4a-6d8bdcac043b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b316efe4abc9f14608db2e61602ac882c7208234
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54958699"
---
# <a name="ngen-support-in-vsix-v3"></a>VSIX v3’te Ngen desteği

(Sürüm 3) uzantı Visual Studio 2017 ve yeni VSIX v3 ile "ngen" biçim, uzantı geliştiricileri artık bildirim derlemelerini yükleme.

"Ngen" ne yaptığını anlatan MSDN kitabından aşağıdadır:

>Native Image Generator (*Ngen.exe*), yönetilen uygulamaların performansını artıran bir araçtır. *Ngen.exe* derlenmiş işlemciye özgü makine kodu içeren dosyalar ve yerel bilgisayarda yerel görüntü önbelleğine yükler yerel görüntüler oluşturur. Çalışma zamanı orijinal derlemeyi derlemek için anlık (JIT) derleyiciyi kullanmak yerine önbellekteki yerel görüntüleri kullanabilir.
>
>gelen [Ngen.exe (yerel Görüntü Oluşturucu)](/dotnet/framework/tools/ngen-exe-native-image-generator)

"Ngen" bir derleme için sırada VSIX "makine başına örnek başına" yüklenmesi gerekir. Bu "tüm kullanıcılar" onay kutusunu işaretleyerek etkin hale getirilebilir `extension.vsixmanifest` Tasarımcısı:

![tüm kullanıcılar](media/check-all-users.png)

## <a name="how-to-enable-ngen"></a>Ngen etkinleştirme

Bir derleme için Ngen etkinleştirmek için kullanabileceğiniz **özellikleri** Visual Studio'daki.

Ayarlanabilir 4 özellikler vardır:

1. **Ngen** (Boolean) - Visual Studio yükleyicisi doğruysa, derleme "ngen" olur.
2. **Ngen uygulaması** (string) - Ngen sağlayan bir uygulama kullanma olanağına *app.config* derleme bağımlılıkları çözümlemek için dosya. Bu değer için bir uygulama özelliği ayarlanmalıdır *app.config* (Visual Studio yükleme dizini göreli) kullanmak istiyorsunuz.
3. **Ngen mimarisi** (enum) - derlemenizi yerel olarak derlemek için Mimari. Seçenekler şunlardır: bir. NotSpecified b. X86 c. X64 d. Tümü
4. **Ngen önceliği** (1 ile 3 arasında tamsayı) - Ngen öncelik düzeyi konumunda belgelenmiştir [Ngen.exe öncelik düzeyleri](/dotnet/framework/tools/ngen-exe-native-image-generator#priority-levels).

İşte göz **özellikleri** eylem penceresinde:

![Ngen özellikleri](media/ngen-in-properties.png)

Bu meta verileri içinde VSIX projenin proje başvurusu ekler *.csproj* dosyası:

```xml
 <ProjectReference Include="..\ClassLibrary1\ClassLibrary1.csproj">
    <Project>{69a979f1-eba2-43e7-9346-0e56e803508b}</Project>
    <Name>ClassLibrary1</Name>
    <Ngen>True</Ngen>
    <NgenApplication>vsn.exe</NgenApplication>
    <NgenArchitecture>X86</NgenArchitecture>
    <NgenPriority>2</NgenPriority>
</ProjectReference>
 ```

 >**Not:** Tercih ederseniz, .csproj dosyasını doğrudan düzenleyebilirsiniz.

## <a name="extra-information"></a>Ek bilgi

Özellik Tasarımcısı değişiklikleri daha fazlasını proje başvuruları için geçerlidir; Ngen meta veri öğeleri için proje içinde ayarlayabilirsiniz (öğeleri .NET derlemeleri gibi uzun yukarıda açıklanan aynı yöntemleri kullanarak).