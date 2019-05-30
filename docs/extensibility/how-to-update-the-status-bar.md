---
title: 'Nasıl yapılır: Durum çubuğunda güncelleştirme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - update status bar
ms.assetid: 7500c8a7-4913-4818-a88b-bfd1b9887cb6
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6f1ba62fc5147eb679e6d6a64685b367aafacae4
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66324791"
---
# <a name="how-to-update-the-status-bar"></a>Nasıl yapılır: Durum Çubuğunu Güncelleştirme
**Durum çubuğu** bir denetim çubuğuna bir veya daha fazla durum metin satırlarını ya da göstergeleri içeren pek çok uygulama penceresi sonunda bulunur.

## <a name="to-update-the-status-bar"></a>Durum çubuğu güncelleştirmek için

1. Uygulama <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser> düzenleyiciniz sağlayan bir form görünümü ve kod görünümü gibi her tek görünüm nesnesinde (DocView).

2. IDE çağırdığında <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A>, bilgilerini **durum çubuğu** yöntemleri çağırarak <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser>.

    > [!NOTE]
    > IDE çağrıları <xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser.SetInfo%2A> yalnızca belge penceresinin başlangıçta etkinleştirildiğinde. Belge penceresinin etkin olduğu süre kalanı için güncelleştirmeniz gerekir **durum çubuğu** Düzenleyicisi değişikliklerinizi durumu bilgileri.

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
- [Durum çubukları](/cpp/mfc/status-bars)