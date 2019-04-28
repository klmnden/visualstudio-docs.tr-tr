---
title: RDT_ReadLock kullanımı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- RDT_ReadLock
- visible
- RDT_EditLock
- invisible
ms.assetid: b935fc82-9d6b-4a8d-9b70-e9a5c5ad4a55
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 04997bfed66da015c4aef82f4741218c88b9ecd1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62859370"
---
# <a name="rdtreadlock-usage"></a>RDT_ReadLock Kullanımı

[_VSRDTFLAGS. RDT_ReadLock](<xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS.RDT_ReadLock>) belge çalıştırılan Belge tablosu (RDT), kilitleme Visual Studio IDE içinde şu anda açık olan tüm belgelerin listesi olduğu için mantıksal sağlayan bir bayrak. Bu bayrak açıldığında belgeleri ve belge kullanıcı arabiriminde görünür veya kilitlerinden bellekte tutulan olup belirler.

Genel olarak, kullandığınız [_VSRDTFLAGS. RDT_ReadLock](<xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS.RDT_ReadLock>) aşağıdakilerden birini olduğunda true:

- Bir belge görünmez açmak istediğiniz ve salt okunur ancak bunu değil, oluşturulan <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> sahip.

- Kullanıcı kullanıcı Arabiriminde görüntülendiğini ve kapatmak çalışıldı önce görünmez açılmış bir belge kaydedilmeyeceğinin sorulması için istediğiniz.

## <a name="how-to-manage-visible-and-invisible-documents"></a>Görünür ve görünmez belgeleri yönetme

Bir kullanıcı kullanıcı Arabiriminde bir belge açıldığında bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> belge için sahip yeniden oluşturulması ve [_VSRDTFLAGS. RDT_EditLock](<xref:Microsoft.VisualStudio.Shell.Interop._VSRDTFLAGS.RDT_EditLock>) bayrağı ayarlanmalıdır. Hayır ise <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> sahibi kurulabilir ve ardından kullanıcı tıkladığında belge kaydedilmeyecek **Tümünü Kaydet** veya IDE'yi kapatır. Bu belge görünmez bellek değiştirilir ve kullanıcı belgeyi Kapat kaydetmenizi veya, kaydedilen açık olup olmadığını anlamına gelir **Tümünü Kaydet** seçilir, ardından bir `RDT_ReadLock` kullanılamaz. Bunun yerine, kullanmanız gereken bir `RDT_EditLock` ve kaydetme bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsDocumentLockHolder> olduğunda bir [__VSREGDOCLOCKHOLDER. RDLH_WeakLockHolder](<xref:Microsoft.VisualStudio.Shell.Interop.__VSREGDOCLOCKHOLDER.RDLH_WeakLockHolder>) bayrağı.

## <a name="rdteditlock-and-document-modification"></a>RDT_EditLock ve Belge değişikliği

Belgenin görünmez açılış verecek bahsedilen önceki bayrağı gösterir, `RDT_EditLock` zaman belge açıldığında kullanıcı tarafından görünür **DocumentWindow**. Bu durumda, kullanıcı ile sunulur bir **Kaydet** ne zaman istemleri görünür **DocumentWindow** kapalı. `Microsoft.VisualStudio.Package.Automation.OAProject.CodeModel` kullanan uygulamaları <xref:Microsoft.VisualStudio.Shell.Interop.IVsInvisibleEditorManager> hizmet başlangıçta iş yalnızca bir `RDT_ReadLock` (yani, belge görünmez bilgileri ayrıştırmak için ne zaman açıldığını) alınır. Belge değiştirilmesi gerekir, daha sonra sonra kilidi için bir zayıf yükseltilir **RDT_EditLock**. Kullanıcı daha sonra belge içinde görünen açarsa **DocumentWindow**, `CodeModel`'s zayıf `RDT_EditLock` serbest bırakılır.

Kullanıcı ardından kapanıyorsa **DocumentWindow** seçerse **Hayır** açık belgeyi kaydetmek isteyip istemediğiniz sorulduğunda sonra `CodeModel` uygulama belgedeki tüm bilgilerin siler ve yeniden açar Belge diskten belge için daha fazla bilgi gerekiyor sonraki açışınızda görünmez. Bu davranış subtlety burada kullanıcının açılır bir örneğidir **DocumentWindow** görünmez açık belgenin değiştirdiği, kapatılan ve sonra seçer **Hayır** belgeyi kaydetmek isteyip istemediğiniz sorulduğunda. Belge varsa, bu durumda bir `RDT_ReadLock`, sonra belgeyi değil gerçekten kapatılacak ve kullanıcı belgeyi kaydedemez seçmiş olsanız da Değiştirilen belgeyi görünmez bellekte açık kalır.

Belgenin görünmez açılış bir zayıf kullanıyorsa `RDT_EditLock`, sonra da kullanıcı ölçeklendirirseniz belge açılır ve başka bir kilit tutulan kilidin verir. Kullanıcının kapattığı zaman **DocumentWindow** seçerse **Hayır** belgeyi kaydetmek isteyip istemediğiniz sorulduğunda sonra belgeyi bellekten kapatılmalıdır. Bu, görünmez istemci bu durum izlemek RDT olayları dinlemeye devam etmesi gereken anlamına gelir. Belge gerekli, sonraki açışınızda, belgenin kapatılıp gerekir.