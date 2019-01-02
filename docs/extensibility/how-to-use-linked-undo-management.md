---
title: 'Nasıl Yapılır: Bağlantılı geri alma yönetimi | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - linked undo management
ms.assetid: af5cc22a-c9cf-45b1-a894-1022d563f3ca
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 639b95909f5d0cf91721760cac27768cb64e477a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53874199"
---
# <a name="how-to-use-linked-undo-management"></a>Nasıl Yapılır: Bağlantılı geri alma Yönetimi'ni kullanın
Bağlantılı geri alma, kullanıcının aynı anda birden fazla dosya aynı düzenlemeleri geri izin verir. Örneğin, bir üstbilgi dosyası ve bir Visual C++ dosya gibi birden fazla program dosyaları arasında eş zamanlı metin değişiklikleri olan bir bağlantılı geri alma işlemi. Bağlantılı geri alma özelliği, geri alma yöneticisi, ortam uygulamasına oluşturulur ve <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLinkedUndoTransactionManager> , bu özelliği ile düzenleme olanak tanır. Bağlantılı geri alma birlikte tek bir geri alma birimi olarak kabul edilmesi için ayrı geri alma yığınlarını bağlayabilirsiniz bir üst geri alma birimi tarafından uygulanır. Kullanarak bağlantılı geri alma yordamı aşağıdaki bölümde ayrıntılı olarak verilmiştir.  
  
## <a name="to-use-linked-undo"></a>Bağlantılı geri alma kullanmak için  
  
1.  Çağrı `QueryService` üzerinde `SVsLinkedUndoManager` işaretçisi almak için `IVsLinkedUndoTransactionManager`.  
  
2.  Çağırarak ilk ana bağlantılı geri alma birimi oluşturma <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLinkedUndoTransactionManager.OpenLinkedUndo%2A>. Bu, bir dizi bağlantılı geri alma yığınlar halinde gruplanması geri alma yığınlarını başlangıç noktasını ayarlar. İçinde `OpenLinkedUndo` yöntemi de gerekecek bağlantılı geri alma katı veya katı olmayan olmasını isteyip istemediğinizi belirtin. Katı olmayan bağlantılı geri alma davranışı ile bağlantılı geri alma eşdüzey belgelerin bazılarına kapatabilirsiniz ve diğer bağlı bırakın geri eşdüzey kendi yığınlarından üzerinde hala anlamına gelir. Katı bağlantılı geri alma davranışını bağlantılı geri alma eşdüzey yığın birlikte ya da hiç geri alınması gerektiğini belirtir. Sonraki bağlantılı geri alma yığınlarını çağırarak ekleme [IOleUndoManager::Add](/windows/desktop/api/ocidl/nf-ocidl-ioleundomanager-add) yöntemi.  
  
3.  Çağrı <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLinkedUndoTransactionManager.CloseLinkedUndo%2A> geri almak için tüm bağlantılı geri alma birimi olarak yedekleyin.  
  
    > [!NOTE]
    >  Bir düzenleyicide bağlantılı geri alma Yönetimi uygulamak için geri alma yönetim ekleyin. Bağlantılı geri alma yönetimini uygulama ile ilgili daha fazla bilgi için bkz: [nasıl yapılır: Uygulama geri alma Yönetim](../extensibility/how-to-implement-undo-management.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCompoundAction>   
 [IOleParentUndoUnit](/windows/desktop/api/ocidl/nn-ocidl-ioleparentundounit)   
 [IOleUndoUnit](/windows/desktop/api/ocidl/nn-ocidl-ioleundounit)   
 [Nasıl yapılır: Uygulama geri alma yönetimi](../extensibility/how-to-implement-undo-management.md)