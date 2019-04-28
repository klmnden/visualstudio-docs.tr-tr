---
title: 'Nasıl yapılır: Durum çubuğunda güncelleştirme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - update status bar
ms.assetid: 7500c8a7-4913-4818-a88b-bfd1b9887cb6
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 1d34642bd805469283ad22d6b40054596ed00a9e
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63441571"
---
# <a name="how-to-update-the-status-bar"></a>Nasıl yapılır: Durum çubuğunda güncelleştirme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**Durum çubuğu** bir denetim çubuğuna bir veya daha fazla durum metin satırlarını ya da göstergeleri içeren pek çok uygulama penceresi sonunda bulunur.  
  
### <a name="to-update-the-status-bar"></a>Durum çubuğu güncelleştirmek için  
  
1. Uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser> düzenleyiciniz sağlayan bir form görünümü ve kod görünümü gibi her tek görünüm nesnesinde (DocView).  
  
2. IDE çağırdığında <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A>, bilgilerini **durum çubuğu** yöntemleri çağırarak <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser>.  
  
    > [!NOTE]
    > IDE çağrıları <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A> yalnızca belge penceresinin başlangıçta etkinleştirildiğinde. Belge penceresinin etkin olduğu süre kalanı için güncelleştirmeniz gerekir **durum çubuğu** Düzenleyicisi değişikliklerinizi durumu bilgileri.  
  
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
