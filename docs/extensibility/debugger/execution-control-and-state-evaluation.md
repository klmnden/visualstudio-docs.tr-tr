---
title: Yürütme denetimi ve durum değerlendirmesi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], execution control
- expression evaluation, control of execution
ms.assetid: 55adde38-1622-4b51-83cb-ce1b04c1ca7a
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bda531e94bdea07ee37eed2b0b79e6f0667ba28e
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66315229"
---
# <a name="execution-control-and-state-evaluation"></a>Yürütme denetimi ve durum değerlendirmesi
Bir uygulamada hata ayıklama işlevlerin içine Adımlama, kesme noktalarında durduruluyor ve yürütme devam böyle yürütme denetimi özelliklerini uygulama gerektirir. Visual Studio hata ayıklama temelleri, yürütme denetimi olayları hata ayıklayıcı bileşenleri arasında gönderilir.

## <a name="in-this-section"></a>Bu bölümde
 [Program denetimi](../../extensibility/debugger/program-control.md) program düzeyinde gerçekleşir aşağıdaki yordamları listeler: sonraki deyimi ayarlamak, yürütme, Adımlama, devam etmeden, askıya alma ve sürdürme.

 [Kesme noktasıyla ilgili metotlar](../../extensibility/debugger/breakpoint-related-methods.md) sınır tanımlar ve Visual Studio'nun desteklediği kesme noktaları tür bekleniyor.

 [Çağrı yığını değerlendirme](../../extensibility/debugger/call-stack-evaluation.md) uygulaması kesme modu sırasında yığın çerçevelerini çağrı yığınının görüntüleme izin yöntemleri ele alınmaktadır.

 [İfade değerlendirme](../../extensibility/debugger/expression-evaluation-visual-studio-debugging-sdk.md) nasıl hata ayıklama altyapısı (DE), ifade değerlendirme (EE) ve oturum hata ayıklama Yöneticisi ayrıştırma ve IDE windows birine girdiğiniz ifade rol oynayan açıklar.

 [Denetim olaylarına](../../extensibility/debugger/control-events.md) denetimli programın yürütülmesi sırasında olayları göndermek için kullanılan arabirimi açıklanır.