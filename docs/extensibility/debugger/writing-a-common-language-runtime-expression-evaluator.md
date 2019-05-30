---
title: Bir ortak dil çalışma zamanı ifade değerlendiricisi yazma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- expression evaluators, tutorial
- expression evaluation, samples
- debugging [Debugging SDK], expression evaluators tutorial
ms.assetid: bd79d57f-8e0a-4e14-a417-0b1de28fa1b2
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c295fcd881ed5348842355846c37af95b725f17e
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66348241"
---
# <a name="writing-a-common-language-runtime-expression-evaluator"></a>Bir ortak dil çalışma zamanı ifade değerlendiricisi yazma
> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için bkz: [CLR ifade değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).

 İfade değerlendiricisi (EE) sözdizimi işleme hata ayıklama altyapısı (DE) ve hata ayıklaması yapılan kod üretilen programlama dilini semantikleri parçasıdır. İfadeler bir programlama dili bağlamında değerlendirilmelidir. Örneğin, bazı dillerde, ' % s'ifadesi "A + B" anlamına gelir "sum a ve b" Diğer dillerde aynı ifadesi "A veya b" gelebilir. Bu nedenle, ayrı bir EE Visual Studio IDE içinde hata ayıklama için nesne kodu oluşturan her programlama dili için yazılmış olmalıdır.

 Visual Studio hata ayıklama paketi bazı yönlerini programlama dilini bağlamında kodu yorumlayan gerekir. Örneğin, ne zaman yürütmeyi durduran içine kullanıcı tarafından yazılan tüm ifadeleri bir kesme noktasında bir **Watch** penceresi değerlendirilir ve görüntülenir. Kullanıcı, bir ifadeyi yazarak yerel değişkenin değerini değiştirebilir bir **Watch** penceresi veya **hemen** penceresi.

## <a name="in-this-section"></a>Bu bölümde
 [Ortak dil çalışma zamanı ve ifade değerlendirme](../../extensibility/debugger/common-language-runtime-and-expression-evaluation.md) Visual Studio bir özel dil bağlamında ifade değerlendirme özellikli EE yazma IDE'ye, özel bir programlama dili tümleştirdiğinizde, açıklar hata ayıklama altyapısı yazmak zorunda kalmadan bir Microsoft Ara dili (MSIL) derlemek sağlar.

 [İfade değerlendirici mimarisi](../../extensibility/debugger/expression-evaluator-architecture.md) gerekli EE arabirimi uygulayan ve ortak dil çalışma zamanı sembol sağlayıcısı (SP) ve bağlayıcı arabirimleri çağırmak nasıl ele alınmaktadır.

 [İfade değerlendiricisi kaydetme](../../extensibility/debugger/registering-an-expression-evaluator.md) EE kendisi ortak dil çalışma zamanı ve çalışma zamanı ortamlarını Visual Studio ile bir sınıf üreteci olarak kaydetmeniz gerekir, notlar.

 [İfade değerlendiricisi uygulama](../../extensibility/debugger/implementing-an-expression-evaluator.md) açıklar nasıl bir ifade değerlendirme işlemi hata ayıklama altyapısı (DE), sembol sağlayıcısı (SP), bağlayıcı nesnesi ve ifade değerlendiricisi (EE) içerir.

 [Yerel görüntüler](../../extensibility/debugger/displaying-locals.md) yürütme durakladığında, hata ayıklama paketi yerel değişkenleri ve bağımsız değişkenler listesini almak için DE çağırması açıklar.

 [Gözcü penceresi ifadesini değerlendirme](../../extensibility/debugger/evaluating-a-watch-window-expression.md) belgeleri nasıl kendi izleme listesindeki her bir ifadenin geçerli değerini belirlemek için DE Visual Studio hata ayıklama paketi çağırır.

 [Yerel bir değiştirin](../../extensibility/debugger/changing-the-value-of-a-local.md) yerel değerinin değiştirilmesi her satırı için Yereller penceresine adını, türünü ve yerel geçerli değerini sağlayan ilişkili nesne olduğunu açıklar.

 [Tür görselleştiricileri ve özel görüntüleyiciler uygulama](../../extensibility/debugger/implementing-type-visualizers-and-custom-viewers.md) hangi arabirim tür görselleştiricileri ve özel görüntüleyiciler desteklemek için hangi bileşen tarafından uygulanması gereken açıklar.

## <a name="see-also"></a>Ayrıca bkz.
 [Visual Studio hata ayıklayıcı genişletilebilirliği](../../extensibility/debugger/visual-studio-debugger-extensibility.md)