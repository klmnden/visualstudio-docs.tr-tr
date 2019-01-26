---
title: Yürütme denetimi ve durum değerlendirmesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], execution control
- expression evaluation, control of execution
ms.assetid: 55adde38-1622-4b51-83cb-ce1b04c1ca7a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e71fb57a4890c29652473338391a0f7181d19ac0
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55010421"
---
# <a name="execution-control-and-state-evaluation"></a>Yürütme denetimi ve durum değerlendirmesi
Bir uygulamada hata ayıklama işlevlerin içine Adımlama, kesme noktalarında durduruluyor ve yürütme devam böyle yürütme denetimi özelliklerini uygulama gerektirir. Visual Studio hata ayıklama temelleri, yürütme denetimi olayları hata ayıklayıcı bileşenleri arasında gönderilir.  
  
## <a name="in-this-section"></a>Bu bölümde  
 [Program denetimi](../../extensibility/debugger/program-control.md)  
 Program düzeyinde gerçekleşir aşağıdaki yordamları listeler: sonraki deyimi ayarlamak, yürütme, Adımlama, devam etmeden, askıya alma ve sürdürme.  
  
 [Kesme noktasıyla ilgili metotlar](../../extensibility/debugger/breakpoint-related-methods.md)  
 Sınır tanımlar ve Visual Studio'nun desteklediği kesme noktaları tür bekleniyor.  
  
 [Çağrı yığını değerlendirme](../../extensibility/debugger/call-stack-evaluation.md)  
 Uygulama kesme modu sırasında yığın çerçevelerini çağrı yığınının görüntülemeyi sağlayan yöntemlerin ele alınmaktadır.  
  
 [İfade değerlendirme](../../extensibility/debugger/expression-evaluation-visual-studio-debugging-sdk.md)  
 Nasıl hata ayıklama altyapısı (DE), ifade değerlendirme (EE) ve oturum hata ayıklama Yöneticisi ayrıştırma dahil olan ve bir ifadenin değerlendirilmesi IDE'nin windows birine girilen açıklanmaktadır.  
  
 [Denetim olayları](../../extensibility/debugger/control-events.md)  
 Denetlenen programın yürütülmesi sırasında olayları göndermek için kullanılan arabirimi açıklanır.