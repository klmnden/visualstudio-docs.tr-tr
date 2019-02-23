---
title: Windows Forms uygulamalarında hata ayıklamak hazırlama | Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging Windows applications
- Windows applications, debugging
- debugging [Visual Studio], Windows applications
- debugging [C#], Windows applications
- debugging [Visual Basic], Windows applications
ms.assetid: 7092ee7f-8378-4def-aef8-1695bd97cf14
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5cc06e33b3549bda9bdc9fe04073ca4cf0d9e9a5
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56679956"
---
# <a name="debugging-preparation-windows-forms-applications"></a>Hata ayıklama hazırlığı: Windows Forms Uygulamaları
Windows Forms proje şablonu, bir Windows Forms uygulaması oluşturur. Bu tür bir uygulamada hata ayıklama [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] oldukça basittir. Daha fazla bilgi için [bir Windows uygulaması projesi oluşturma](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/42wc9kk5(v=vs.100)).

 Proje şablonuyla bir Windows Forms projesi oluşturduğunuzda [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] hata ayıklama ve yayın yapılandırmaları için gereken ayarları otomatik olarak oluşturur. Gerekirse, bu ayarları değiştirebilirsiniz. Bu ayarlar değiştirilebilir  **\<proje adı > özellik sayfaları** iletişim kutusu (**Projem** Visual Basic'te).

 Daha fazla bilgi için [önerilen özellik ayarları](../debugger/managed-debugging-recommended-property-settings.md).

 Aşağıdaki tabloda bir ek önerilen özellik ayarı görüntüler.

### <a name="configuration-properties-in-debug-tab"></a>Hata ayıklama sekmesindeki yapılandırma özellikleri

|**Özellik adı**|**Ayarı**|
|-----------------------|-----------------|
|**Başlatma eylemi**|-Kümesine **başlangıç projesi** çoğu zaman. Kümesine **harici program Başlat** başka bir yürütülebilir başlatmak istiyorsanız başlattığınızda hata ayıklama (genellikle DLL'lerinde hata ayıklama için).|

 Windows Forms uygulamaları içinde hata ayıklama [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)], veya zaten çalışan bir uygulamaya ekleme. Ekleme hakkında daha fazla bilgi için bkz. [çalışan işlemlere ekleme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md).

### <a name="to-debug-a-c-f-or-visual-basic-windows-forms-application"></a>Hata ayıklamak için bir C#, F#, veya Visual Basic Windows Forms uygulaması

1. Projeyi [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].

2. Kesme noktaları, gerektiği şekilde oluşturun.

    Windows Forms uygulamaları, olay temelli olduğundan, kesme noktalarınız olay işleyici kodu veya olay işleyici kodu tarafından çağrılan yöntemler geçer. Kesme noktaları yerleştirmek için tipik olaylar şunlardır:

   1. ' A tıklayın, Enter vb. gibi bir denetim ile ilişkili olayları.

   2. Uygulama başlatma ve kapatma, yük, etkin, vb. gibi ilişkili olaylar.

   3. Odak ve doğrulama olayları.

      Daha fazla bilgi için [Windows Forms'ta olay işleyicileri oluşturma](/dotnet/framework/winforms/creating-event-handlers-in-windows-forms).

3. Üzerinde **hata ayıklama** menüsünde tıklatın **Başlat**.

4. İçinde açıklanan teknikleri kullanarak hata ayıklama [hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md).

## <a name="see-also"></a>Ayrıca Bkz.
- [Yönetilen Kodda Hata Ayıklama](../debugger/debugging-managed-code.md)
- [C#, F# ve Visual Basic Proje Türleri](../debugger/debugging-preparation-csharp-f-hash-and-visual-basic-project-types.md)
- [Nasıl yapılır: Hata Ayıklama ve Dağıtım Yapılandırmalarını Ayarlama](../debugger/how-to-set-debug-and-release-configurations.md)
- [C# Hata Ayıklama Yapılandırması Proje Ayarları](../debugger/project-settings-for-csharp-debug-configurations.md)
- [Visual Basic Hata Ayıklama Yapılandırması Proje Ayarları](../debugger/project-settings-for-a-visual-basic-debug-configuration.md)
- [Çalıştırma İşlemine İliştirme](../debugger/attach-to-running-processes-with-the-visual-studio-debugger.md)
- [Windows Forms](/dotnet/framework/winforms/index)