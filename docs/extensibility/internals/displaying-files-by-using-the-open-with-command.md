---
title: Komutu ile Aç'ı kullanarak dosyaları görüntüleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- project types, supporting Open With command
- Open With command
- persistence, supporting Open With command
ms.assetid: 53794bc3-1b73-4d40-954e-cfade1abddcf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b3d8c9873f529a366f7910946cf5807c45f73ca7
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63415380"
---
# <a name="display-files-by-using-the-open-with-command"></a>Birlikte Aç komutunu kullanarak dosyaları görüntüleme
Bir proje görüntülemek için IDE sorabilir **birlikte Aç** iletişim kutusu. Bu istek standart düzenleyicileri seçimi sahip bir dosyayı açmak için kullanıcıya sorar. Aşağıdaki adımlar, bu işlemi açıklanmaktadır:

1. Proje çağrıları <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.OpenStandardEditor%2A>, değerini belirterek `OSE_UseOpenWithDialog` için `OSEOpenDocEditor` parametresi.

2. Belgenin dosya adı uzantısına bağlı olarak, IDE kayıt defteri can listelenen hangi düzenleyicileri belirtilen belgeyi açmayı belirler ve bu bilgiyi görüntüler **birlikte Aç** iletişim kutusu.

    > [!NOTE]
    > İçinde içermesi gereken bir iç Düzenleyicisi olan projelerin **birlikte Aç** iletişim kutusu için böyle bir düzenleyici her bir düzenleyici fabrikası kaydetmeniz gerekir. İç düzenleyiciler yalnızca işlev uygulamasında zorlanan proje, belirli bir türü ile birlikte <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> yöntemi. IDE, temel metin düzenleyicisi ve ikili düzenleyicide yerleşik Düzenleyici fabrikası sahiptir. IDE da bir düzenleyici fabrikası adına her kayıtlı Windows dosya ilişkilendirmesi örneği oluşturur. Microsoft Word gibi bir dosya örneğidir.

3. Kullanıcının seçtiği bir öğeden hemen sonra **birlikte Aç** çağırarak belge açılır iletişim kutusu, IDE'yi ardından <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.OpenStandardEditor%2A> yöntemi. Daha fazla bilgi için [nasıl yapılır: Standart düzenleyicileri açma](../../extensibility/how-to-open-standard-editors.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Açın ve proje öğeleri Kaydet](../../extensibility/internals/opening-and-saving-project-items.md)
- [Dosya Aç komutunu kullanarak dosyaları görüntüleme](../../extensibility/internals/displaying-files-by-using-the-open-file-command.md)
- [Nasıl yapılır: Açık standart düzenleyicileri](../../extensibility/how-to-open-standard-editors.md)
