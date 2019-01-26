---
title: 'Nasıl yapılır: Durum çubuğunda güncelleştirme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - update status bar
ms.assetid: 7500c8a7-4913-4818-a88b-bfd1b9887cb6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 49661e379c81bac935e2d2ae2279e32d548eb698
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54929883"
---
# <a name="how-to-update-the-status-bar"></a>Nasıl yapılır: Durum çubuğunda güncelleştirme
**Durum çubuğu** bir denetim çubuğuna bir veya daha fazla durum metin satırlarını ya da göstergeleri içeren pek çok uygulama penceresi sonunda bulunur.  
  
## <a name="to-update-the-status-bar"></a>Durum çubuğu güncelleştirmek için  
  
1.  Uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser> düzenleyiciniz sağlayan bir form görünümü ve kod görünümü gibi her tek görünüm nesnesinde (DocView).  
  
2.  IDE çağırdığında <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A>, bilgilerini **durum çubuğu** yöntemleri çağırarak <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser>.  
  
    > [!NOTE]
    >  IDE çağrıları <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A> yalnızca belge penceresinin başlangıçta etkinleştirildiğinde. Belge penceresinin etkin olduğu süre kalanı için güncelleştirmeniz gerekir **durum çubuğu** Düzenleyicisi değişikliklerinizi durumu bilgileri.  
  
## <a name="robust-programming"></a>Güçlü programlama  
 A **durum çubuğu** dört ayrı alanları içerir:  
  
- Durum metni  
  
- İlerleme çubuğu  
  
- Animasyonlu simgesi  
  
- Düzenleyici bilgileri  
  
  Daha fazla bilgi için [durum çubukları](/cpp/mfc/status-bars).  
  
  IDE otomatik olarak çağıran <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A> yöntemi, <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser> belge penceresinin etkinleştirildiğinde, uygulama.  
  
  VSPackage'ı uygulayan, durum çubuğundaki durum metni güncelleştirmekten sorumludur. Durum metin alanı boş metin olarak ayarlanmışsa "Hazır" Bu dizeye IDE sıfırlar ("") boşta kalma zaman.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Durum çubukları](/cpp/mfc/status-bars)