---
title: Kullanıcıya geri bildirim | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- user model feedback
- environment, context
- IDE, context
- IDE, user feedback
ms.assetid: 2d472a24-3813-4f5f-9783-b491ad8a71ad
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 7773c611733ccec525fc25264311e72c1dfe36e2
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54755624"
---
# <a name="feedback-to-the-user"></a>Kullanıcıya Geri Bildirim
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

İçinde [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] tümleşik geliştirme ortamı (IDE), kullanıcının geçerli seçimi ve genel seçim bağlamını ilgili kullanılabilir işlevler temel görsel geri bildirim. Aşağıdaki tabloda farklı seçim bağlamlarında kullanılabilir olan işlevleri listeler.  
  
|Seçim bağlamı|Kullanılabilir işlevleri|  
|-----------------------|-----------------------------|  
|IDE|Global|  
|Geçerli ürün kümesi|Belirli bir ürün|  
|Etkin olan hiyerarşi|Hiyerarşi türü özel|  
|Etkin olan hiyerarşi öğesi|Hiyerarşi öğesi türü özel|  
|Etkin belge|Belge türü özel|  
|En üstteki Çok Belgeli Arabirim (MDI) penceresi|Pencere türü özel|  
|Geçerli seçim bağlamı|Seçim bağlamını belirli|  
  
 Yalnızca kullanıcılar gereken ve sürekli olarak tutarlı seçimi ve ortam bağlamı geri bildirim sağlamak işlevselliğini yüzey, IDE karmaşıklığını azaltın. Her bir pencere IDE içinde açıldığında aşağıdaki kurallar geçerlidir:  
  
- Pencerenin alt seçim bağlamını değişirse, seçim geri bildirimi penceresinde açıkça belirtilir ve dinamik Yardım penceresi, geçerli bağlam yansıtacak şekilde güncelleştirilir yoksa.  
  
- Pencerenin genel seçim bağlamını değişirse, tüm özel bağlam menüleri, etkin olan hiyerarşi pencere ve uygulama başlık çubuğunun geçerli bağlam yansıtacak şekilde güncelleştirilir.  
  
- Pencerenin geçerli seçimde özelliklerini yüzey **özellikleri** penceresi ve isteğe bağlı olarak gösteriliyorsa, **özellik sayfaları** iletişim kutusu.  
  
- Pencere özellikleri surface etmez veya genel seçim bağlamını değiştirme, artık IDE'de etkin pencere olduğunda seçim geri bildirimi penceresinde kalmalıdır değil.  
  
- Tüm belge özel araç pencereleri, sürekli olarak etkin belgeyi yansıtmalıdır.  
  
- Menüleri ve araç çubukları uygulama başlık çubuğunda en üstteki Çok Belgeli Arabirim (MDI) istemci penceresi yansıtmalıdır.  
  
  Örneğin, zaman içinde bir Visual Basic Web uygulaması projesini Web formu HTML görünümü açılır ve kullanıcının seçtiği bir `<td>` etiketi, geri bildirim aşağıdaki şekilde sağlanır:  
  
- Seçimi etkin pencerede gösterilir ve yansıtılan **özellikleri** penceresi.  
  
- Belgeye özgü **araç kutusu** etkin belgeyi yansıtacak şekilde güncelleştirilir.  
  
- **Düzenleyicisi** araç ve **tablo** menüsü görüntülenir ve Web formu pencerenin yansıtmak için başlık çubuğunda güncelleştirir.  
  
- Genellikle etkin olan hiyerarşi penceresinde **Çözüm Gezgini**ve geçerli bağlamı ve bağlama duyarlı yansıtmak için başlık çubuğunda güncelleştirme **proje** menü komutları, etkin Web şimdi Uygula Uygulama projesi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Seçim ve para birimi IDE](../../extensibility/internals/selection-and-currency-in-the-ide.md)   
 [Seçim bağlamı nesneleri](../../extensibility/internals/selection-context-objects.md)   
 [Hiyerarşiler ve Seçim](../../extensibility/internals/hierarchies-and-selection.md)
