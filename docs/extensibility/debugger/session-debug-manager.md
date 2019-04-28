---
title: Hata ayıklama oturumu Manager | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- session debug manager, unifying session views
- session debug manager, broadcasting
- debugging [Debugging SDK], session debug manager
- session debug manager
- session debug manager, debug engine multiplexing
- session debug manager, delegating
ms.assetid: fbb1928d-dddc-43d1-98a4-e23b0ecbae09
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: edbb1510265307e1c9fe6c8a01cffc0115d879ac
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62864271"
---
# <a name="session-debug-manager"></a>Oturum hata ayıklama Yöneticisi
Oturum hata ayıklama Yöneticisi (SDM) makineleri herhangi bir sayıda arasında herhangi bir sayıda birden çok işlem programlarında hata ayıklama hata ayıklama altyapısı (DE) herhangi bir sayıda yönetir. SDM çoğaltıcı bir hata ayıklama altyapısı olmaya ek olarak, IDE için hata ayıklama oturumu birleşik bir görünümünü sağlar.

## <a name="session-debug-manager-operation"></a>Oturum hata ayıklama Yöneticisi işlemi
 Oturum hata ayıklama Yöneticisi (SDM) DE yönetir. Çalıştıran bir makinede aynı anda birden fazla hata ayıklama altyapısı olabilir. DEs çoğullamalısınız için SDM DEs arabirimlerden sayısı sarmalar ve bunları tek bir arabirim olarak IDE sunar.

 Performansı artırmak için bazı arabirimler multiplexed değildir. Bunun yerine, doğrudan DE kullanılan ve bu arabirimler çağrıları SDM geçmez. Özel yönerge, bellek veya belirli bir program tarafından belirli bir DE hata ayıklaması belgede başvurduğundan Örneğin, bellek, kod ve belge bağlamı ile kullanılan arabirimleri, multiplexed değildir. Diğer bir DE iletişim, düzeyinde yer alması gerekir.

 Bu tüm içeriklerde geçerli değildir. İfade değerlendirme bağlamı arabirimi çağrılar SDM gidin. SDM ifadesi değerlendirmesi sırasında sarmalar [IDebugExpression2](../../extensibility/debugger/reference/idebugexpression2.md) ifade değerlendirildiğinde, programlar olabilir aynı işlemde hata ayıklama birden çok DEs gerektirebilir bulunduğundan IDE verir arabirimi aynı iş parçacığında çalışır.

 SDM genellikle bir temsilci mekanizması olarak görev yapar, ancak bir yayın mekanizması davranan. Örneğin, ifade değerlendirmesi sırasında SDM tüm DEs, belirtilen bir iş parçacığında kod çalıştırabilir bildirmek için bir yayın mekanizması görevi görür. Benzer şekilde, SDM durdurma olayı aldığında, bunların çalışmasını durdurmanız program yayınlar. Bir adım çağrıldığında SDM programlar çalışmaya devam ettiğini yayınlar. Kesme noktaları ayrıca her DE olarak yayınlanır.

 SDM geçerli programı, iş parçacığı veya yığın çerçevesi izlemez. İşlem, program ve iş parçacığı bilgisi SDM belirli hata ayıklama olayları ile birlikte gönderilir.

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md)
- [Hata ayıklayıcı bileşenleri](../../extensibility/debugger/debugger-components.md)
- [Hata ayıklayıcı bağlamları](../../extensibility/debugger/debugger-contexts.md)