---
title: Programlar | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], programs
- programs, debugging
ms.assetid: e1f955d8-95da-493b-837e-e97741a26d7e
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 62bd59222fa8b173f3e805f60f4b8bd3ad245c6f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53964630"
---
# <a name="programs"></a>Programlar
Hata ayıklayıcı mimarisinde bir *program*:  
  
-   Bir modül kümesini ve iş parçacıkları kümesi için bir kapsayıcıdır. Bir program yok tek benzerleme Windows işletim sisteminde vardır.  
  
     Bir program bir alt türüdür. Örneğin, bir Web sitesi ayıklanırken bir komut dosyası bir program olarak görülebilir. Bir komut dosyası komut dosyası altyapısı işlemde çalışırken, bağımsız olarak diğer betikleri, ayrıca kendi iş parçacıkları kümesine sahiptir. Hata ayıklama altyapısı (DE), bir programa ve bir işlem veya iş parçacığı ekler.  
  
-   Kendisi ve onu çalışan işlemi tanımlayabilirsiniz. Bir program, gelen ayrılmış ve varsa, oluşturulan DE açıklamak için eklenebilir. Bir program de yürütme, Durdur, devam olması ve sonlandırıldı.  
  
-   Tüm iş parçacıklarının sıralayabilirsiniz. Bir program kendi Ayrıştırılmış kod akış aynı zamanda sağlayabilir ve belirli belge konumlarından tüm kod bağlamları sıralayabilirsiniz.  
  
-   Tarafından temsil edilen bir [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md) program bağlanmadan önce veya bağlı uygulama Ekle işleminin bir parçası olarak oluşturulan arabirimi. Bir bağlantı noktası program bir işlemin sıraladığında her program karşılık gelen uygun olarak oluşturulur [IDebugProgramNode2](../../extensibility/debugger/reference/idebugprogramnode2.md) arabirimi geçirilen bağımsız değişken olarak [AddProgramNode](../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md). Hata ayıklama altyapısı ayrıca oluştururken `IDebugProgram2` arabirimleri programları, bu programlar göstermek için bir program düğüm uygun olarak oluşturulmaz. `IDebugProgramNode2` Bir DE tarafından oluşturulan arabirimleri kullanılan gerçek hata ayıklama için bir bağlantı noktası tarafından oluşturulanlar yalnızca hangi programların bir işlemde çalışan keşfetmek için kullanılırken.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [İşlemler](../../extensibility/debugger/processes.md)   
 [Program düğümleri](../../extensibility/debugger/program-nodes.md)   
 [Modüller](../../extensibility/debugger/modules.md)   
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)   
 [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md)   
 [Belge konumu](../../extensibility/debugger/document-position.md)   
 [Kod bağlamı](../../extensibility/debugger/code-context.md)   
 [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugProgramNode2](../../extensibility/debugger/reference/idebugprogramnode2.md)   
 [AddProgramNode](../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md)