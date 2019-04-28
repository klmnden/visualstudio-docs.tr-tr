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
ms.openlocfilehash: bd04cfa1e271f94f1b37aa0fbd62e9b846d9a70d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62925718"
---
# <a name="execution-control-and-state-evaluation"></a>Yürütme denetimi ve durum değerlendirmesi
Bir uygulamada hata ayıklama işlevlerin içine Adımlama, kesme noktalarında durduruluyor ve yürütme devam böyle yürütme denetimi özelliklerini uygulama gerektirir. Visual Studio hata ayıklama temelleri, yürütme denetimi olayları hata ayıklayıcı bileşenleri arasında gönderilir.

## <a name="in-this-section"></a>Bu bölümde
 [Program denetimi](../../extensibility/debugger/program-control.md) program düzeyinde gerçekleşir aşağıdaki yordamları listeler: sonraki deyimi ayarlamak, yürütme, Adımlama, devam etmeden, askıya alma ve sürdürme.

 [Kesme noktasıyla ilgili metotlar](../../extensibility/debugger/breakpoint-related-methods.md) sınır tanımlar ve Visual Studio'nun desteklediği kesme noktaları tür bekleniyor.

 [Çağrı yığını değerlendirme](../../extensibility/debugger/call-stack-evaluation.md) uygulaması kesme modu sırasında yığın çerçevelerini çağrı yığınının görüntüleme izin yöntemleri ele alınmaktadır.

 [İfade değerlendirme](../../extensibility/debugger/expression-evaluation-visual-studio-debugging-sdk.md) nasıl hata ayıklama altyapısı (DE), ifade değerlendirme (EE) ve oturum hata ayıklama Yöneticisi ayrıştırma ve IDE windows birine girdiğiniz ifade rol oynayan açıklar.

 [Denetim olaylarına](../../extensibility/debugger/control-events.md) denetimli programın yürütülmesi sırasında olayları göndermek için kullanılan arabirimi açıklanır.