---
title: 'İş Akışı Tasarımcısı - nasıl yapılır: Bir İş Akışı Projesine Yeni Öğe Ekleme'
ms.date: 06/25/2018
ms.topic: conceptual
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
ms.assetid: 5c6180ca-af10-4513-b0cb-7d478fd84eab
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f0e5df48d1c96905c022a6737d58f75d6c548ccb
ms.sourcegitcommit: 159ed9d4f56cdc1dff2fd19d9dffafe77e46cd4e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53738695"
---
# <a name="how-to-add-a-new-item-to-a-workflow-project"></a>Nasıl Yapılır: Bir iş akışı projesine yeni öğe ekleme

Bir iş akışı projesi oluşturduktan sonra iş akışı etkinlikleri, tasarımcılar ve diğer tanıdık Visual Studio öğelerini projenize ekleyebilirsiniz.

Aşağıdaki tabloda, bir iş akışı projesine eklediğiniz Windows Workflow Foundation (WF) öğeleri listeler:


| Ad | Açıklama |
|-| - |
| Etkinlik | Diğer etkinliklerini oluşmasına bir etkinlik. Bu öğeyi seçerseniz ekler aynı XAML dosyasını projeye seçerken elde edebilirsiniz gibi **etkinlik Kitaplığı** için yeni bir proje şablonu. Hakkında daha fazla bilgi için bu yordamı, bkz: [bir iş akışı projesi oluşturma](creating-a-workflow-project.md). |
| Etkinlik Tasarımcısı | Bir etkinliğin tasarım zamanı deneyimi özelleştirmek için bir tasarımcı. Bu öğeyi seçerseniz ekler aynı dosyaları projeye seçerken elde edebilirsiniz gibi **etkinlik Tasarımcısı Kitaplığı** için yeni bir proje şablonu. |
| Kod etkinliği | Yürütme mantığı kod olarak yazılmış bir etkinlik. Bir kaynak kodu dosyası geçersiz kılma ile <xref:System.Activities.CodeActivity.Execute%2A> yöntemi zaten oluşturulan sizin için. |
| WCF iş akışı hizmeti | A [!INCLUDE[indigo2](../workflow-designer/includes/indigo2_md.md)] iş akışı etkinlikleri kullanılarak yapılmış bir hizmet. Bu öğeyi seçerseniz ekler aynı dosyaları projeye seçerken elde edebilirsiniz gibi **WCF iş akışı hizmeti uygulaması** için yeni bir proje şablonu. Bu yordam hakkında daha fazla bilgi için bkz. [nasıl yapılır: WCF iş akışı hizmeti uygulaması oluşturma](/visualstudio/workflow-designer/creating-a-workflow-project). |

## <a name="to-add-a-new-item-to-a-workflow-project"></a>Bir iş akışı projesine yeni bir öğe eklemek için

1. Üzerinde **proje** menüsünde **Yeni Öğe Ekle**.

   **Yeni Öğe Ekle** iletişim kutusu açılır.

1. Sol bölmede seçin **iş akışı** kategoriye ve iş akışı öğesi şablonu seçin.

   > [!NOTE]
   > Görmüyorsanız **iş akışı** kategori, ilk yükleme **Windows Workflow Foundation** Visual Studio 2017'in bileşeni. Ayrıntılı yönergeler için bkz. [Windows Workflow Foundation'ı yükleme](developing-applications-with-the-workflow-designer.md#install-windows-workflow-foundation).

1. Öğe için bir ad girin **adı** iletişim kutusunun alt kısmındaki kutusu.

1. Seçin **Ekle** projeye öğe eklemek için.

## <a name="see-also"></a>Ayrıca bkz.

- [Bir iş akışı projesi oluşturma](../workflow-designer/creating-a-workflow-project.md)