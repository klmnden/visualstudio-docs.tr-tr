---
title: Özel Parametreler | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- wizards, custom parameters
- custom parameters
ms.assetid: ba5c364b-66e6-47ea-9760-a0b70de8f0a0
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: c8c243490a88010031bad91d6b45fe5645d21e6e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53826367"
---
# <a name="custom-parameters"></a>Özel Parametreler
Bir sihirbaz başlatıldıktan sonra özel parametreler sihirbaz işlemi denetleyin. İlgili *.vsz* dosyası tümleşik geliştirme ortamı (IDE) paketlenir ve Sihirbazı başlattığınızda sihirbaz dize dizisi geçirilen kullanıcı tanımlı parametre dizisi sağlar. Sihirbaz dizisini ayrıştırır ve gerçek işlem sihirbazın denetlemek için bu bilgileri kullanır. Bu şekilde, bir sihirbaz işlevselliği içeriğine bağlı olarak özelleştirebilirsiniz *.vsz* dosya.  
  
 Sihirbazı başlattığınızda bağlam parametreleri, diğer taraftan, proje durumunu tanımlar. Daha fazla bilgi için [bağlam parametreleri](../../extensibility/internals/context-parameters.md).  
  
 Aşağıdaki örneğidir bir *.vsz* özel parametreleri olan dosyası:  
  
```  
VSWIZARD 8.0  
Wizard=VsWizard.VsWizard_Engine  
Param="WIZARD_NAME = Sample Wizard"  
Param="WIZARD_UI = FALSE"  
Param="RELATIVE_PATH = VSWizards\Classwiz\ATL"  
Param="PREPROCESS_FUNCTION = CanAddATLSupport"  
Param="PROJECT_TYPE = CSPROJ"  
```  
  
 Yazarı *.vsz* dosyası parametrelerinin değerlerini ekler. Bir kullanıcı seçtiğinde **yeni proje** veya **Yeni Öğe Ekle** üzerinde **dosya** menüsü veya bir projeye sağ tıklayarak **Çözüm Gezgini**, IDE Bu değerleri dize dizisi toplar. IDE sonra projenin çağırır <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3.AddItem%2A> yöntemiyle <xref:Microsoft.VisualStudio.Shell.Interop.VSADDITEMOPERATION> bayrak kümesi ve proje çağrıları <xref:EnvDTE.IVsExtensibility.RunWizardFile%2A> Sihirbazı'nı çalıştıran ve sonucu döndürerek sorumlu yöntemi.  
  
 Sihirbaz, dize dizisi, ayrıştırma ve dizeleri uygun şekilde hareket sorumludur. Özel Parametreler uygulayarak bu şekilde, çeşitli işlevler gerçekleştiren bir sihirbaz oluşturabilirsiniz. Diğer bir deyişle, bir sihirbaz üç farklı olabilir *.vsz* dosyaları. Her dosya, farklı çeşitli durumlarda sihirbazda davranışını denetlemek için özel parametreleri kümesini geçirir.  
  
 Daha fazla bilgi için [sihirbaz (.vsz) dosyası](../../extensibility/internals/wizard-dot-vsz-file.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject3>   
 [Bağlam parametreleri](../../extensibility/internals/context-parameters.md)   
 [Sihirbazlar](../../extensibility/internals/wizards.md)   
 [Sihirbaz (.vsz) dosyası](../../extensibility/internals/wizard-dot-vsz-file.md)