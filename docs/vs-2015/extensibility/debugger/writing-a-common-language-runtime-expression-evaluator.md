---
title: Bir ortak dil çalışma zamanı ifade değerlendiricisi yazma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- expression evaluators, tutorial
- expression evaluation, samples
- debugging [Debugging SDK], expression evaluators tutorial
ms.assetid: bd79d57f-8e0a-4e14-a417-0b1de28fa1b2
caps.latest.revision: 24
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 961a4d646a61fedda381f9451902b3bcdcc956d6
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63435271"
---
# <a name="writing-a-common-language-runtime-expression-evaluator"></a>Ortak Dil Çalışma Zamanı İfade Değerlendiricisi Yazma
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

> [!IMPORTANT]
> Visual Studio 2015'te, bu şekilde ifade değerlendiricisi uygulama kullanım dışı bırakılmıştır. CLR ifade değerlendiricisi uygulama hakkında daha fazla bilgi için lütfen bkz [CLR ifade Değerlendiricilerini](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) ve [yönetilen ifade değerlendiricisi örnek](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 İfade değerlendiricisi (EE) sözdizimi işleme hata ayıklama altyapısı (DE) ve hata ayıklaması yapılan kod üretilen programlama dilini semantikleri parçasıdır. İfadeler bir programlama dili bağlamında değerlendirilmelidir. Örneğin, bazı dillerde, ' % s'ifadesi "A + B" anlamına gelir "sum a ve b" Diğer dillerde aynı ifadesi "A veya b" gelebilir. Bu nedenle, ayrı bir EE Visual Studio IDE içinde hata ayıklama için nesne kodu oluşturan her programlama dili için yazılmış olmalıdır.  
  
 Visual Studio hata ayıklama paketi bazı yönlerini programlama dilini bağlamında kodu yorumlayan gerekir. Örneğin, ne zaman yürütmeyi durduran içine kullanıcı tarafından yazılan tüm ifadeleri bir kesme noktasında bir **Watch** penceresi değerlendirilir ve görüntülenir. İçinde bir ifade yazarak kullanıcı yerel bir değişken değerini de değiştirebilir bir **Watch** penceresi veya **hemen** penceresi.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [Ortak Dil Çalışma Zamanı ve İfade Değerlendirme](../../extensibility/debugger/common-language-runtime-and-expression-evaluation.md)  
 Visual Studio IDE'ye özel programlama dilini tümleştirdiğinizde bir EE yazma özel dil ifadeleri bağlam içinde değerlendirme yeteneğine bir Microsoft Ara dili (MSIL) derleme olanak açıklar hata ayıklama altyapısı yazmak zorunda kalmadan.  
  
 [İfade Değerlendirici Mimarisi](../../extensibility/debugger/expression-evaluator-architecture.md)  
 Gerekli EE arabirimi uygulayan ve ortak dil çalışma zamanı sembol sağlayıcısı (SP) ve bağlayıcı arabirimleri çağırmak nasıl ele alınmaktadır.  
  
 [İfade Değerlendiricisi Kaydetme](../../extensibility/debugger/registering-an-expression-evaluator.md)  
 EE kendisi ortak dil çalışma zamanı ve çalışma zamanı ortamlarını Visual Studio ile bir sınıf üreteci olarak kaydetmeniz gerekir, notlar.  
  
 [ifade Değerlendiricisi Uygulama](../../extensibility/debugger/implementing-an-expression-evaluator.md)  
 Bir ifade değerlendirme işlemi, hata ayıklama altyapısı (DE), sembol sağlayıcısı (SP), bağlayıcı nesnesi ve ifade değerlendiricisi (EE) nasıl içerir açıklar.  
  
 [Yerel Öğeleri Görüntüleme](../../extensibility/debugger/displaying-locals.md)  
 Yürütme durakladığında, hata ayıklama paketi yerel değişkenleri ve bağımsız değişkenler listesini almak için DE çağırması açıklar.  
  
 [Gözcü Penceresi İfadesini Değerlendirme](../../extensibility/debugger/evaluating-a-watch-window-expression.md)  
 Visual Studio hata ayıklama paketi kendi izleme listesindeki her bir ifadenin geçerli değerini belirlemek için DE çağırması belgeler.  
  
 [Yerel Bir Öğenin Değerini Değiştirme](../../extensibility/debugger/changing-the-value-of-a-local.md)  
 Yerel bir değerinin değiştirilmesi her satırı için Yereller penceresine adını, türünü ve yerel geçerli değerini sağlayan ilişkili nesne olduğunu açıklar.  
  
 [Tür Görselleştiricileri ve Özel Görüntüleyiciler Uygulama](../../extensibility/debugger/implementing-type-visualizers-and-custom-viewers.md)  
 Hangi arabirim tür görselleştiricileri ve özel görüntüleyiciler desteklemek için hangi bileşen tarafından uygulanması gereken açıklar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Hata Ayıklayıcı Genişletilebilirliği](../../extensibility/debugger/visual-studio-debugger-extensibility.md)
