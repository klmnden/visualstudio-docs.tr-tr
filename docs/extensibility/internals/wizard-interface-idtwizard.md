---
title: Sihirbaz arabirimi (IDTWizard) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- IDTWizard interface
- wizards, interface
ms.assetid: 09618d9d-d115-45b6-bccc-de328994b39c
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 16ce767c70e532da5991b99a5a77f65b7adc12e0
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53869732"
---
# <a name="wizard-interface-idtwizard"></a>Sihirbaz Arabirimi (IDTWizard)
Tümleşik geliştirme ortamı (IDE) kullanan <xref:EnvDTE.IDTWizard> sihirbazları ile iletişim kurmak için arabirim. Sihirbazlar, IDE'de yüklenmesi için bu arabirimi uygulamalıdır.  
  
 <xref:EnvDTE.IDTWizard.Execute%2A> Yöntemi ile ilişkili tek yöntemdir <xref:EnvDTE.IDTWizard> arabirimi. Sihirbaz bu yöntemi uygulaması ve IDE arabirimi yöntemini çağırır. Aşağıdaki örnekte, yöntem imzasını gösterir.  
  
```  
/* IDTWizard Method */  
STDMETHOD(Execute)(THIS_  
   /* [in] */ IDispatch *Application,  
   /* [in] */ long hwndOwner,  
   /* [in] */ SAFEARRAY * *ContextParams,  
   /* [in] */ SAFEARRAY * *CustomParams,  
   /* [out] [in] */ wizardResult *RetVal  
   );  
```  
  
 Başlangıç mekanizması için her ikisi de benzer **yeni proje** ve **Yeni Öğe Ekle** sihirbazları. Ya da başlamak için çağrı <xref:EnvDTE.IDTWizard> Dteinternal.h içinde tanımlanan arabirimi. Tek fark, bağlam ve arabirimi çağrıldığında arabirimine geçirilen özel parametreleri kümesidir.  
  
 Aşağıdaki bilgiler açıklar <xref:EnvDTE.IDTWizard> sihirbazları çalışacak şekilde uygulamalıdır arabirimi [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE. IDE çağrıları <xref:EnvDTE.IDTWizard.Execute%2A> aşağıdaki Geçirme Sihirbazı, yöntemi:  
  
-   DTE nesnesi  
  
     DTE nesnesi Otomasyon modeli köküdür.  
  
-   Kod kesimi içinde gösterildiği pencere iletişim kutusu için bir tanıtıcı `hwndOwner ([in] long)`.  
  
     Bu sihirbaz kullanır `hwndOwner` Sihirbazı iletişim kutusu için üst öğe olarak.  
  
-   Bağlam parametreleri geçirilen arabirimi değişken için bir SAFEARRAY'i kod kesimi gösterildiği `[in] SAFEARRAY (VARIANT)* ContextParams`.  
  
     Bağlam parametreleri Başlatılmakta olan sihirbaz türü için belirli değerler dizisi ve proje geçerli durumunu içerir. IDE bağlam parametreleri Sihirbazına geçirir. Daha fazla bilgi için [bağlam parametreleri](../../extensibility/internals/context-parameters.md).  
  
-   Özel Parametreler geçirilen arabirimi bir değişken için bir SAFEARRAY'i kod kesimi gösterildiği gibi `[in] SAFEARRAY (VARIANT)* CustomParams`.  
  
     Özel Parametreler, kullanıcı tarafından tanımlanan parametre dizisi içerir. .Vsz dosyası IDE özel parametrelerini geçirir. Değerler tarafından belirlenir `Param=` deyimleri. Daha fazla bilgi için [özel parametreler](../../extensibility/internals/custom-parameters.md).  
  
-   Arabirim dönüş değerleri  
  
    ```  
    wizardResultSuccess = -1,  
    wizardResultFailure = 0  
    wizardResultCancel = 1  
    wizardResultBackout = 2  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Bağlam parametreleri](../../extensibility/internals/context-parameters.md)   
 [Özel Parametreler](../../extensibility/internals/custom-parameters.md)   
 [Sihirbazlar](../../extensibility/internals/wizards.md)   
 [Sihirbaz (.Vsz) Dosyası](../../extensibility/internals/wizard-dot-vsz-file.md)