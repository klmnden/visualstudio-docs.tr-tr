---
title: Gerekli olayları gönderme | Microsoft Docs
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
- debugging [Debugging SDK], required events
ms.assetid: 08319157-43fb-44a9-9a63-50b919fe1377
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 154157a8de67cd1bef8fd489b3c1fc7406a05629
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49303678"
---
# <a name="sending-the-required-events"></a>Gerekli Olayları Gönderme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Gerekli olayları göndermek için bu yordamı kullanın.  
  
## <a name="process-for-sending-required-events"></a>Gerekli olayları gönderme işlemi  
 Aşağıdaki olaylar, bu sıralamayı oluşturmak bir hata ayıklama altyapısı, (DE) ve programa ekleme gereklidir:  
  
1.  Gönderme bir [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md) oturum hata ayıklama Yöneticisi (SDM) DE bir işlem bir veya daha fazla programlarında hata ayıklama başlatıldığında olay nesnesiyle.  
  
2.  Ayıklanacak programın bağlı olduğu zaman Gönder bir [IDebugProgramCreateEvent2](../../extensibility/debugger/reference/idebugprogramcreateevent2.md) SDM olay nesnesiyle. Bu olay altyapısı tasarımınızın bağlı olarak bir durdurma olay olabilir.  
  
3.  Program ekli ise işlem başlatıldığında Gönder bir [IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md) SDM yeni iş parçacığının IDE bildirmek üzere Olay nesnesiyle. Bu olay altyapısı tasarımınızın bağlı olarak bir durdurma olay olabilir.  
  
4.  Gönderme bir [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md) ayıklanan programa tamamlanan yükleme veya programa ekleme tamamlandığında olduğunda SDM olay nesnesiyle. Bu olay bir durdurma olay olmalıdır.  
  
5.  Ayıklanacak uygulama başlatılmışsa, gönderme bir [IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md) çalıştırılmak üzere çalışma zamanı mimarisi kod ilk yönerge olduğunda SDM olay nesnesiyle. Bu olay her zaman bir durdurma olayıdır. Hata ayıklama oturumu Adımlama, IDE üzerinde bu olaya durdurur.  
  
> [!NOTE]
>  Birçok dil kodlarını başında genel başlatıcıların veya harici, önceden derlenmiş işlevleri (CRT kitaplığı veya _ana) kullanın. Programın hata ayıkladığınız dil önce ilk giriş noktası öğelerin bu türlerinden birini içeriyorsa, daha sonra bu kodu çalıştırmak ve giriş noktası olayı gönderilir, kullanıcı giriş noktanız, gibi **ana** veya `WinMain`, ulaşıldı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Bir Programı Hataları Ayıklanacak Şekilde Etkinleştirme](../../extensibility/debugger/enabling-a-program-to-be-debugged.md)

