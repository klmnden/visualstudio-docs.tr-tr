---
title: Eski API'yi kullanarak metin katmanları erişme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - text layers
ms.assetid: 2258fcdd-38d1-479d-b8f8-1d4e6525f72c
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 975e8624a6ffbfe0c5ae7544f2b978487465e34e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68148017"
---
# <a name="accessing-text-layers-by-using-the-legacy-api"></a>Eski API'yi Kullanarak Metin Katmanlarına Erişme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Metin katmanı, genellikle bazı yönlerini metin düzenini kapsüller. Örneğin, "işlevi--bir zamanda" katman metin önce ve sonra giriş işaretinin (ekleme noktası metni) içeren bir işlev gizliyor.  
  
 Arabellek ve bir görünüm arasında metin katmanı bulunur ve görünümü arabellek içeriği görür şeklini değiştirir.  
  
## <a name="text-layer-information"></a>Metin katmanı bilgileri  
 Aşağıdaki listede, metin katmanları nasıl çalıştığı açıklanmaktadır [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]:  
  
- Metin katmanındaki metin söz dizimi renklendirme ve işaretçileri ile donatılmış.  
  
- Şu anda kendi katmanları uygulayamaz.  
  
- Kullanıma sunan bir katmana <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer>, türetilen <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines>. Metin arabelleği, ayrıca temel alınan katmanlarla polymorphically yarayan bir görünüm sağlayan bir katman olarak uygulanır.  
  
- Görünüm ve arabellek arasında herhangi bir sayıda katmanları şekilde. Her katman yalnızca aşağıdaki katman ile ilgilidir ve görünüm büyük ölçüde en üst katman ile ilgilidir. (Görünüm arabellek hakkında bazı bilgiler yok.)  
  
- Bir katman altında olan katmanları etkileyebilir. Bu standart olayları kaynaklanan ötesinde üzerindeki katmanların etkilemez.  
  
- Düzenleyici'de, gizli metin ve yapay metin kaydırmayı katmanları olarak uygulanır. Gizli ve yapay metin katmanları ile doğrudan etkileşim olmadan uygulayabilirsiniz. Daha fazla bilgi için [eski dil hizmetinde ana hat oluşturmayı](../extensibility/internals/outlining-in-a-legacy-language-service.md) ve <xref:Microsoft.VisualStudio.TextManager.Interop.IVsSyntheticTextSession>.  
  
- Her metin katmanı aracılığıyla kullanıma kendi yerel koordinat sistemini sahip <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer> arabirimi. Temel alınan metin arabelleğini tek bir satır içerebilir ancak satır kaydırma katmanı, örneğin, iki satır içerebilir.  
  
- Görünüm katmanları iletişim kurar <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLayeredTextView> arabirimi. Bu arabirim görünümü koordinatları arabellek koordinatları ile mutabık kılmak için kullanın.  
  
- Kaynaklı metin yapay metin katmanı, bir yerel uygulaması sağlamalısınız gibi tüm katman <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer.CreateTrackingPoint%2A>.  
  
- Yanında <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLayer>, metin katmanı uygulamalıdır <xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer> ve olayları yangın <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLinesEvents> arabirimi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özel düzenleyicilerde söz dizimi renklendirmesi](../extensibility/syntax-coloring-in-custom-editors.md)   
 [Metin işaretçileri eski API'si ile kullanma](../extensibility/using-text-markers-with-the-legacy-api.md)   
 [Eski API'yi Kullanarak Düzenleyici Denetimlerini ve Menüleri Özelleştirme](../extensibility/customizing-editor-controls-and-menus-by-using-the-legacy-api.md)
