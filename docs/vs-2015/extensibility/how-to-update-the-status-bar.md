---
title: 'Nasıl yapılır: durum çubuğunda güncelleştirme | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - update status bar
ms.assetid: 7500c8a7-4913-4818-a88b-bfd1b9887cb6
caps.latest.revision: 13
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f19b6c46615a41f25c5a9f3b979f1a1eed36b25f
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49948506"
---
# <a name="how-to-update-the-status-bar"></a>Nasıl yapılır: durum çubuğunda güncelleştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**Durum çubuğu** bir denetim çubuğuna bir veya daha fazla durum metin satırlarını ya da göstergeleri içeren pek çok uygulama penceresi sonunda bulunur.  
  
### <a name="to-update-the-status-bar"></a>Durum çubuğu güncelleştirmek için  
  
1.  Uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser> düzenleyiciniz sağlayan bir form görünümü ve kod görünümü gibi her tek görünüm nesnesinde (DocView).  
  
2.  IDE çağırdığında <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A>, bilgilerini **durum çubuğu** yöntemleri çağırarak <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser>.  
  
    > [!NOTE]
    >  IDE çağrıları <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A> yalnızca belge penceresinin başlangıçta etkinleştirildiğinde. Belge penceresinin etkin olduğu süre kalanı için güncelleştirmeniz gerekir **durum çubuğu** Düzenleyicisi değişikliklerinizi durumu bilgileri.  
  
## <a name="robust-programming"></a>Güçlü Programlama  
 A **durum çubuğu** dört ayrı alanları içerir:  
  
- Durum metni  
  
- İlerleme çubuğu  
  
- Animasyonlu simgesi  
  
- Düzenleyici bilgileri  
  
  Daha fazla bilgi için [durum çubukları](http://msdn.microsoft.com/library/fcbc5029-1aab-4e14-adf7-419038a4935e).  
  
  IDE otomatik olarak çağıran <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A> yöntemi, <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser> belge penceresinin etkinleştirildiğinde, uygulama.  
  
  VSPackage'ı uygulayan, durum çubuğundaki durum metni güncelleştirmekten sorumludur. Durum metin alanı boş metin olarak ayarlanmışsa "Hazır" Bu dizeye IDE sıfırlar ("") boşta kalma zaman.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Durum Çubukları](http://msdn.microsoft.com/library/fcbc5029-1aab-4e14-adf7-419038a4935e)

