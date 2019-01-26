---
title: Program düğümleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- program nodes, debugging context
- debugging [Debugging SDK], program nodes
- program nodes, adding
- program nodes, superceding
ms.assetid: 1c5a5c13-c14d-42c3-af11-4c63f1032c8d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 61e09651786870d892eaa85a01561ddb283785bf
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54921901"
---
# <a name="program-nodes"></a>Program düğümleri
Hata ayıklayıcı mimarisinde bir *program düğüm*:  
  
- Basit bir program açıklamasıdır.  
  
- Kendisi ve onu çalışan işlemi tanımlayabilirsiniz. Öğesinden ayrıldı ve varsa, oluşturulan hata ayıklama altyapısı (DE) tanımlamak için bir program düğümü eklenebilir.  
  
- Tarafından temsil edilen bir [IDebugProgramNode2](../../extensibility/debugger/reference/idebugprogramnode2.md) arabirimi, genellikle DE veya bağlantı noktası tarafından oluşturulur. Program düğümleri çağırarak bir bağlantı noktasına eklenir [AddProgramNode](../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md). Bir program düğüm bir bağlantı eklendiğinde bu programı bu düğümün temsil ettiği program içeren işleme eklenir.  
  
  Süre bir hata ayıklama oturumu, hata ayıklama paketi bağlı olarak uygulama başlatıldıktan sonra program düğümleri karşılık gelen programlar oluşturmak için kullanılır. Bir işlem için programları sorgulandığında programları numaralandırılır, program her düğüm için bir tane.  
  
  Bir program iliştirildiği önce IDE program basit bir açıklamasını gerekir. Bu bilgi programı düğümden elde edilebilir. Program için bağlandıktan sonra IDE programdaki tüm iş parçacıkları listesi gibi daha ayrıntılı bilgileri görüntüler. Bu bilgiler programından elde edilir.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Programlar](../../extensibility/debugger/programs.md)   
 [İşlemler](../../extensibility/debugger/processes.md)   
 [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md)   
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)   
 [IDebugProgramNode2](../../extensibility/debugger/reference/idebugprogramnode2.md)   
 [AddProgramNode](../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md)