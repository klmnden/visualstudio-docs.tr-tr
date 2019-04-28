---
title: Program denetimi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], control of execution
ms.assetid: 6be80904-e66c-4cae-8891-1113b799fb01
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 8102bc488d5c74f751fb93584016aa6904fbe2d9
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63438078"
---
# <a name="program-control"></a>Program Denetimi
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Visual Studio'da hata ayıklama, tüm aşağıdaki adımlama ve yordamları devam program düzeyinde gerçekleşir:  
  
- Sonraki deyimin ayarlanması, diğer bir deyişle, bilgisayarınızı belirli çerçeve ortamında yürütülecek sonraki yönergesi için ayarlama  
  
- Yürütme, Adımlama modundan çıkmak diğer bir deyişle, devam  
  
- Sonraki yönergeyi Adımlama  
  
- Geçerli bir atlama modu ile devam etme  
  
- Program tarafından bulunan iş parçacıklarını askıya alma  
  
- Program tarafından bulunan iş parçacıklarını sürdürme  
  
> [!NOTE]
> Çağrı yığınını görüntüleme iş parçacığı düzeyinde uygulanır. Bir iş parçacığı için çağrı yığınını görüntülerken çerçeve bilgileri numaralandırmak için tüm yöntemleri uygulamalıdır [IEnumDebugFrameInfo2](../../extensibility/debugger/reference/ienumdebugframeinfo2.md) arabirimi.  
  
## <a name="methods-of-program-control"></a>Program denetiminin yöntemleri  
 Aşağıdaki tabloda yöntemlerini gösterilmektedir [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md) , uygulanmalı en düşük düzeyde işlev hata ayıklama altyapısı (DE) ve yürütme denetimi için.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IDebugProgram2::Execute](../../extensibility/debugger/reference/idebugprogram2-execute.md)|Durdurulmuş bir program tarafından bulunan tüm iş parçacığı çalışmaya devam eder. Yürütme denetimi için gereklidir.|  
|[IDebugProgram2::Continue](../../extensibility/debugger/reference/idebugprogram2-continue.md)|Durdurulmuş bir program tarafından bulunan tüm iş parçacığı çalışmaya devam eder. Yürütme denetimi için gereklidir.|  
|[IDebugProgram2::Step](../../extensibility/debugger/reference/idebugprogram2-step.md)|Bir adım belirli bir iş parçacığı üzerinde gerçekleştirir. Program tarafından bulunan tüm diğer iş parçacıklarını çalışmaya devam eder. Yürütme denetimi için gereklidir.|  
  
 Çok iş parçacıklı programlarda, ayrıca uygulamalıdır [IDebugProgram2::EnumThreads](../../extensibility/debugger/reference/idebugprogram2-enumthreads.md) yöntemi ve tüm yöntemleri [IEnumDebugThreads2](../../extensibility/debugger/reference/ienumdebugthreads2.md) arabirimi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yürütme Denetimi ve Durum Değerlendirmesi](../../extensibility/debugger/execution-control-and-state-evaluation.md)
