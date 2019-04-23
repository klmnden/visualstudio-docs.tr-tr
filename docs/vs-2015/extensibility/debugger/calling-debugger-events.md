---
title: Hata ayıklayıcı olayları çağırma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], events
ms.assetid: b3440ac3-80af-40c6-bef4-cbf00fa67885
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 2f162affe2324afaa8fb1d506c3177311386bfc1
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60110355"
---
# <a name="calling-debugger-events"></a>Hata Ayıklayıcısı Olaylarını Çağırma
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklama oturumları, olayları belirli bir sırayla oluşur.  
  
## <a name="discussion"></a>Tartışma  
 Hata ayıklama altyapısı (DE) ve oturum hata ayıklama Yöneticisi (SDM) arasındaki çağrıların desenini anlamak için tipik hata ayıklama oturumunda gerçekleşen olaylara arama sırası şunları gösterir:  
  
1. [Ekleme ve programdan ayırma](../../extensibility/debugger/attaching-and-detaching-to-a-program.md)  
  
2. [Hata ayıklayıcı başlatılıyor](../../extensibility/debugger/launching-the-debugger.md)  
  
3. [Program sonlandırma](../../extensibility/debugger/terminating-a-program.md)  
  
4. [Bir kesme noktası oluşturma](../../extensibility/debugger/creating-a-breakpoint.md)  
  
5. [Ne zaman bir kesme noktası bağlar veya ilişkisiz olma](../../extensibility/debugger/when-a-breakpoint-binds-or-becomes-unbound.md)  
  
6. [Kesme noktası hataları](../../extensibility/debugger/breakpoint-errors.md)  
  
7. [Kesme noktasına ulaşma](../../extensibility/debugger/hitting-a-breakpoint.md)  
  
8. [Kesme noktasını silme](../../extensibility/debugger/deleting-a-breakpoint.md)  
  
9. [Kesme moduna girme](../../extensibility/debugger/entering-break-mode.md)  
  
10. [Kesme modunda Adımlama](../../extensibility/debugger/stepping-in-break-mode.md)  
  
11. [Kesme modunda ifade değerlendirme](../../extensibility/debugger/expression-evaluation-in-break-mode.md)  
  
12. [Özel durum işleme](../../extensibility/debugger/exception-handling-visual-studio-sdk.md)  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özel Hata Ayıklama Altyapısı Oluşturma](../../extensibility/debugger/creating-a-custom-debug-engine.md)
