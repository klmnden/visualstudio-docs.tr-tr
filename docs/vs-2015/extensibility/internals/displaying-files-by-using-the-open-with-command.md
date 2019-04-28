---
title: Komutu ile Aç'ı kullanarak dosyaları görüntüleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- project types, supporting Open With command
- Open With command
- persistence, supporting Open With command
ms.assetid: 53794bc3-1b73-4d40-954e-cfade1abddcf
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: de43b6c4f441f8c6bde2d6c248274aed3937a7ee
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63408804"
---
# <a name="displaying-files-by-using-the-open-with-command"></a>Birlikte Aç Komutunu Kullanarak Dosyaları Görüntüleme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir proje görüntülemek için IDE sorabilir **birlikte Aç** iletişim kutusu. Bu istek standart düzenleyicileri seçimi sahip bir dosyayı açmak için kullanıcıya sorar. Aşağıdaki adımlar, bu işlemi açıklanmaktadır.  
  
1. Proje çağrıları <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.OpenStandardEditor%2A>, için OSE_UseOpenWithDialog değerini belirterek `OSEOpenDocEditor` parametresi.  
  
2. Belgenin dosya adı uzantısına bağlı olarak, IDE kayıt defteri can listelenen hangi düzenleyicileri belirtilen belgeyi açmayı belirler ve bu bilgiyi görüntüler **birlikte Aç** iletişim kutusu.  
  
    > [!NOTE]
    > İçinde içermesi gereken bir iç Düzenleyicisi olan projelerin **birlikte Aç** iletişim kutusu için böyle bir düzenleyici her bir düzenleyici fabrikası kaydetmeniz gerekir. İç düzenleyiciler yalnızca işlev uygulamasında zorlanan proje, belirli bir türü ile birlikte <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory.CreateEditorInstance%2A> yöntemi. IDE, temel metin düzenleyicisi ve ikili düzenleyicide yerleşik Düzenleyici fabrikası sahiptir. IDE da bir düzenleyici fabrikası adına her kayıtlı Windows dosya ilişkilendirmesi örneği oluşturur. Microsoft Word gibi bir dosya örneğidir.  
  
3. Kullanıcının seçtiği bir öğeden hemen sonra **birlikte Aç** çağırarak belge açılır iletişim kutusu, IDE'yi ardından <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShellOpenDocument.OpenStandardEditor%2A> yöntemi. Daha fazla bilgi için [nasıl yapılır: Standart düzenleyicileri açma](../../extensibility/how-to-open-standard-editors.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Açma ve proje öğelerini kaydetme](../../extensibility/internals/opening-and-saving-project-items.md)   
 [Dosya Aç komutunu kullanarak dosyaları görüntüleme](../../extensibility/internals/displaying-files-by-using-the-open-file-command.md)   
 [Nasıl yapılır: Standart Düzenleyiciler Açma](../../extensibility/how-to-open-standard-editors.md)
