---
title: RDT_ReadLock kullanımı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- RDT_ReadLock
- visible
- RDT_EditLock
- invisible
ms.assetid: b935fc82-9d6b-4a8d-9b70-e9a5c5ad4a55
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: c818023d50b733a4818c87e67d0b49abde518ad2
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54765796"
---
# <a name="rdtreadlock-usage"></a>RDT_ReadLock Kullanımı
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

<xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS> bir belge çalıştırılan Belge tablosu (RDT), kilitleme Visual Studio IDE içinde şu anda açık olan tüm belgelerin listesi olduğu için mantıksal sağlayan bayrak değeridir. Bu bayrak açıldığında belgeleri ve belge kullanıcı arabiriminde görünür veya kilitlerinden bellekte tutulan olup belirler.  
  
 Genellikle, kullanacağınız <xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS> aşağıdakilerden birini olduğunda true:  
  
-   Görünmez bir belgeyi açmaya istediğinizde ve salt okunur ancak değil ancak hangi kurulan <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> sahip.  
  
-   Kullanıcı önce kullanıcı görünmez açılmış bir belge kaydedilmeyeceğinin sorulması için istediğiniz zaman kullanıcı Arabiriminde görüntülenen ve kapatmak çalışıldı.  
  
## <a name="how-to-manage-visible-and-invisible-documents"></a>Görünür ve görünmez belgeleri yönetme  
 Bir kullanıcı kullanıcı Arabiriminde bir belge açıldığında bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> belge için sahip yeniden oluşturulması ve <xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS> bayrağı ayarlanmalıdır. Hayır ise <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> sahibi kurulabilir ve ardından kullanıcı tıkladığında belge kaydedilmeyecek **Tümünü Kaydet** veya IDE'yi kapatır. Bu belge görünmez bellek değiştirilir ve kullanıcı belgeyi Kapat kaydetmenizi veya, kaydedilen açık olup olmadığını anlamına gelir **Tümünü Kaydet** seçilir, ardından bir `RDT_ReadLock` kullanılamaz. Bunun yerine, kullanmanız gereken bir `RDT_EditLock` ve kaydetme bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsDocumentLockHolder> olduğunda bir <xref:Microsoft.VisualStudio.Shell.Interop.__VSREGDOCLOCKHOLDER> bayrağı.  
  
## <a name="rdteditlock-and-document-modification"></a>RDT_EditLock ve Belge değişikliği  
 Belgenin görünmez açılış verecek bahsedilen önceki bayrağı gösterir, `RDT_EditLock` zaman belge açıldığında kullanıcı tarafından görünür **DocumentWindow**. Bu durumda, kullanıcı ile sunulur bir **Kaydet** ne zaman istemleri görünür **DocumentWindow** kapalı. Kullanan Microsoft.VisualStudio.Package.Automation.OAProject.CodeModel uygulamaları <xref:Microsoft.VisualStudio.Shell.Interop.IVsInvisibleEditorManager> hizmet başlangıçta iş yalnızca bir `RDT_ReadLock` (yani, belge görünmez bilgileri ayrıştırmak için ne zaman açıldığını) alınır. Belge değiştirilmesi gerekir, daha sonra sonra kilidi için bir zayıf yükseltilir **RDT_EditLock**. Kullanıcı daha sonra belge içinde görünen açarsa **DocumentWindow**, `CodeModel`'s zayıf `RDT_EditLock` serbest bırakılır.  
  
 Kullanıcı ardından kapanıyorsa **DocumentWindow** seçerse **Hayır** açık belgeyi kaydetmek isteyip istemediğiniz sorulduğunda sonra `CodeModel` uygulama belgedeki tüm bilgilerin siler ve yeniden açar Belge diskten belge için daha fazla bilgi gerekiyor sonraki açışınızda görünmez. Bu davranış subtlety burada kullanıcının açılır bir örneğidir **DocumentWindow** görünmez açık belgenin değiştirdiği, kapatılan ve sonra seçer **Hayır** belgeyi kaydetmek isteyip istemediğiniz sorulduğunda. Belge varsa, bu durumda bir `RDT_ReadLock`, sonra belgeyi değil gerçekten kapatılacak ve kullanıcı belgeyi kaydedemez seçmiş olsanız da Değiştirilen belgeyi görünmez bellekte açık kalır.  
  
 Belgenin görünmez açılış bir zayıf kullanıyorsa `RDT_EditLock`, sonra da kullanıcı ölçeklendirirseniz belge açılır ve başka bir kilit tutulan kilidin verir. Kullanıcının kapattığı zaman **DocumentWindow** seçerse **Hayır** belgeyi kaydetmek isteyip istemediğiniz sorulduğunda sonra belgeyi bellekten kapatılmalıdır. Bu, görünmez istemci bu durum izlemek RDT olayları dinlemeye devam etmesi gereken anlamına gelir. Belge gerekli, sonraki açışınızda, belgenin kapatılıp gerekir.
