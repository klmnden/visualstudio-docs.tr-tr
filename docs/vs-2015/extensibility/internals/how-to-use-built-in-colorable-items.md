---
title: 'Nasıl yapılır: Yerleşik renklendirilebilir öğeleri kullanma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- colorable items
- language services, built-in colorable items
ms.assetid: 5e5f3436-6bad-4fd2-8823-6a30353ba648
caps.latest.revision: 18
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 21a2b520111c07b6c964eae19f5a6064e926db70
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60039989"
---
# <a name="how-to-use-built-in-colorable-items"></a>Nasıl yapılır: Yerleşik Renklendirilebilir Öğeleri Kullanma
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Yerleşik renklendirilebilir öğeleri kullanmadan önce öncelikle tümleşik geliştirme ortamı (IDE), bu durumda, kendi özel renklendirilebilir öğeler sağlamıyorsunuz sinyal gerekir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsProvideColorableItems> nesneleri. Dil hizmeti bir kayıt defteri anahtarını ayarlayarak bunu yapabilirsiniz.  
  
### <a name="to-use-built-in-colorable-items"></a>Yerleşik renklendirilebilir öğeleri kullanmak için  
  
1. HKEY_LOCAL_MACHINE\VisualStudio altında\\*X.Y*\Languages\Language Hizmetleri\\*dil adı*burada *X.Y* sürümüdür[!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] ve *dil adı* adı adlı bir DWORD kayıt defteri girdisinin değeri, dili, oluşturma `RequestStockColors`.  
  
2. Ayarlama `RequestStockColors` kayıt defteri girdisinin değeri 1.  
  
     Kayıt defteri girişinin, uygulamanızın Renklendirici oluşturduktan sonra <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.ColorizeLine%2A> yöntemi üyelerinin kullanabilir <xref:Microsoft.VisualStudio.TextManager.Interop.DEFAULTITEMS> renk öznitelikleri ' Düzenleyicisi tarafından kullanılmak üzere bir dizi doldurmak için sabit listesi.  
  
    > [!NOTE]
    >  Özel renklendirilebilir öğeler sağlıyorsanız bu kayıt defteri girdisi ayarlamayın. Daha fazla bilgi için [özel renklendirilebilir öğeler](../../extensibility/internals/custom-colorable-items.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özel düzenleyicilerde söz dizimi renklendirmesi](../../extensibility/syntax-coloring-in-custom-editors.md)   
 [Eski dil hizmetinde söz dizimi renklendirmesi](../../extensibility/internals/syntax-coloring-in-a-legacy-language-service.md)   
 [Söz dizimi renklendirmesi uygulama](../../extensibility/internals/implementing-syntax-coloring.md)   
 [Özel renklendirilebilir öğeler](../../extensibility/internals/custom-colorable-items.md)   
 [Eski Dil Hizmeti Kaydetme](../../extensibility/internals/registering-a-legacy-language-service2.md)
