---
title: Bir ortak dil çalışma zamanı ifade değerlendiricisi yazma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- expression evaluators, tutorial
- expression evaluation, samples
- debugging [Debugging SDK], expression evaluators tutorial
ms.assetid: bd79d57f-8e0a-4e14-a417-0b1de28fa1b2
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7026a0851288a87a291f3312aa2a955049bb3a39
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54926949"
---
# <a name="writing-a-common-language-runtime-expression-evaluator"></a>Bir ortak dil çalışma zamanı ifade değerlendiricisi yazma
> [!IMPORTANT]
>  Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için bkz: [CLR ifade değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 İfade değerlendiricisi (EE) sözdizimi işleme hata ayıklama altyapısı (DE) ve hata ayıklaması yapılan kod üretilen programlama dilini semantikleri parçasıdır. İfadeler bir programlama dili bağlamında değerlendirilmelidir. Örneğin, bazı dillerde, ' % s'ifadesi "A + B" anlamına gelir "sum a ve b" Diğer dillerde aynı ifadesi "A veya b" gelebilir. Bu nedenle, ayrı bir EE Visual Studio IDE içinde hata ayıklama için nesne kodu oluşturan her programlama dili için yazılmış olmalıdır.  
  
 Visual Studio hata ayıklama paketi bazı yönlerini programlama dilini bağlamında kodu yorumlayan gerekir. Örneğin, ne zaman yürütmeyi durduran içine kullanıcı tarafından yazılan tüm ifadeleri bir kesme noktasında bir **Watch** penceresi değerlendirilir ve görüntülenir. Kullanıcı, bir ifadeyi yazarak yerel değişkenin değerini değiştirebilir bir **Watch** penceresi veya **hemen** penceresi.  
  
## <a name="in-this-section"></a>Bu bölümde  
 [Ortak dil çalışma zamanı ve ifade değerlendirme](../../extensibility/debugger/common-language-runtime-and-expression-evaluation.md)  
 Visual Studio IDE'ye özel programlama dilini tümleştirdiğinizde bir EE yazma özel dil ifadeleri bağlam içinde değerlendirme yeteneğine bir Microsoft Ara dili (MSIL) derleme olanak açıklar hata ayıklama altyapısı yazmak zorunda kalmadan.  
  
 [İfade değerlendirici mimarisi](../../extensibility/debugger/expression-evaluator-architecture.md)  
 Gerekli EE arabirimi uygulayan ve ortak dil çalışma zamanı sembol sağlayıcısı (SP) ve bağlayıcı arabirimleri çağırmak nasıl ele alınmaktadır.  
  
 [İfade değerlendiricisi kaydetme](../../extensibility/debugger/registering-an-expression-evaluator.md)  
 EE kendisi ortak dil çalışma zamanı ve çalışma zamanı ortamlarını Visual Studio ile bir sınıf üreteci olarak kaydetmeniz gerekir, notlar.  
  
 [İfade değerlendiricisi uygulama](../../extensibility/debugger/implementing-an-expression-evaluator.md)  
 Bir ifade değerlendirme işlemi, hata ayıklama altyapısı (DE), sembol sağlayıcısı (SP), bağlayıcı nesnesi ve ifade değerlendiricisi (EE) nasıl içerir açıklar.  
  
 [Görüntü yerel öğeler](../../extensibility/debugger/displaying-locals.md)  
 Yürütme durakladığında, hata ayıklama paketi yerel değişkenleri ve bağımsız değişkenler listesini almak için DE çağırması açıklar.  
  
 [Gözcü penceresi ifadesini değerlendirme](../../extensibility/debugger/evaluating-a-watch-window-expression.md)  
 Visual Studio hata ayıklama paketi kendi izleme listesindeki her bir ifadenin geçerli değerini belirlemek için DE çağırması belgeler.  
  
 [Yerel bir değiştirin](../../extensibility/debugger/changing-the-value-of-a-local.md)  
 Yerel bir değerinin değiştirilmesi her satırı için Yereller penceresine adını, türünü ve yerel geçerli değerini sağlayan ilişkili nesne olduğunu açıklar.  
  
 [Tür görselleştiricileri ve özel görüntüleyiciler uygulama](../../extensibility/debugger/implementing-type-visualizers-and-custom-viewers.md)  
 Hangi arabirim tür görselleştiricileri ve özel görüntüleyiciler desteklemek için hangi bileşen tarafından uygulanması gereken açıklar.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Visual Studio hata ayıklayıcı genişletilebilirliği](../../extensibility/debugger/visual-studio-debugger-extensibility.md)