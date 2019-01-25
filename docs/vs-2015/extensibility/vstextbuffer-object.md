---
title: VSTextBuffer nesnesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
f1_keywords:
- VSTextBuffer
helpviewer_keywords:
- VSTextBuffer object, reference
- views [Visual Studio SDK], VSTextBuffer object
ms.assetid: c5f94b45-7249-4e1f-a53d-1d2a1c61e0ef
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 94e58b8af799dba44bd2563ee6c404c3cdcb3583
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54763508"
---
# <a name="vstextbuffer-object"></a>VSTextBuffer Nesnesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Metin arabelleği nesnesini bir akış genellikle bir dosya ile ilişkilendirilmiş bir Unicode metin temsil eder. A <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer> nesne gibi bir Sihirbazı söz konusu olduğunda çekirdek Düzenleyici, bağlamı dışında kullanılabilir.  
  
 Aşağıdaki tabloda, arabirimler gösterilir `VSTextBuffer`.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IOleCommandTarget](http://msdn.microsoft.com/library/windows/desktop/ms683797)|Standart OLE arabirimidir. Esas olarak, Geri Al/Yinele arabellekteki işleme için kullanılır.|  
|[IPersistFile](http://msdn.microsoft.com/library/windows/desktop/ms687223)|Standart OLE arabirimidir.|  
|[IPersistStream](http://msdn.microsoft.com/library/windows/desktop/ms690091)|Standart OLE arabirimidir.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsCompoundAction>|Bileşimden eylemleri (diğer bir deyişle, bir tek geri al/Yinele biriminde gruplandırılır eylemleri) oluşturulmasını sağlar.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData>|Metin arabelleği tarafından yönetilen belge veri kalıcılığını etkinleştirir.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer>|Temel hizmetleri sağlar. birden çok istemci tarafından kullanılır.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextFind>|Arabellek aramak için kullanılır.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines>|Sağlar okuma ve yazma iki boyutlu koordinatlarını kullanarak özellikleri. Devralınan `IVsTextBuffer`.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextStream>|Sağlar okuma ve yazma özellikleri kullanarak tek boyutlu koordinatları. Devralınan `IVsTextBuffer`.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextScanner>|Hızlı, arabellekteki metni akışa dayalı olarak sıralı erişim sağlar.|  
|<xref:Microsoft.VisualStudio.TextManager.Interop.IVsUserData>|Genel Özellikler koleksiyonu erişim sağlar. En önemli özellik adını veya bilinen ad, arabellek olur. Bir GUID oluşturma ve bir anahtar olarak kullanarak rastgele verilerinizi bu arabirimle arabellek depolayabilirsiniz.|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer>|Bağlantı noktaları için olayları destekler.|  
  
## <a name="remarks"></a>Açıklamalar  
 `VSTextBuffer` Genellikle tarafından bulunan bir `QueryInterface` çağırmak `IVsTextBuffer`. Daha fazla bilgi için [metin arabelleğini](../extensibility/accessing-the-text-buffer-by-using-the-legacy-api.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView>   
 [Şekil Düzenle](http://msdn.microsoft.com/f08872bd-fd9c-4e36-8cf2-a2a2622ef986)
