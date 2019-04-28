---
title: Kullanıcıya geri bildirim | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- user model feedback
- environment, context
- IDE, context
- IDE, user feedback
ms.assetid: 2d472a24-3813-4f5f-9783-b491ad8a71ad
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4503639e65650b70871c9bf23a26eac1d4892a5f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62909998"
---
# <a name="feedback-to-the-user"></a>Kullanıcıya geri bildirim
İçinde [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı (IDE), kullanıcının geçerli seçimi ve genel seçim bağlamını ilgili kullanılabilir işlevler temel görsel geri bildirim. Aşağıdaki tabloda farklı seçim bağlamlarında kullanılabilir olan işlevleri listeler.

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

- Pencerenin alt seçim bağlamını değişirse, seçim geri bildirimi penceresinde açıkça belirtilir ve **dinamik Yardım** penceresinde gösterilen, güncelleştirildiğinde geçerli bağlam yansıtacak şekilde.

- Pencerenin genel seçim bağlamını değişirse, tüm özel bağlam menüleri, etkin olan hiyerarşi pencere ve uygulama başlık çubuğunun geçerli bağlam yansıtacak şekilde güncelleştirilir.

- Pencerenin geçerli seçimde özelliklerini yüzey **özellikleri** penceresi ve isteğe bağlı olarak gösteriliyorsa, **özellik sayfaları** iletişim kutusu.

- Pencere özellikleri surface etmez veya genel seçim bağlamını değiştirme, artık IDE'de etkin pencere olduğunda seçim geri bildirimi penceresinde kalmalıdır değil.

- Tüm belge özel araç pencereleri, sürekli olarak etkin belgeyi yansıtmalıdır.

- Menüleri ve araç çubukları uygulama başlık çubuğunda en üstteki Çok Belgeli Arabirim (MDI) istemci penceresi yansıtmalıdır.

  Örneğin, HTML görüntülediğinizde bir **Web formu** içindeki Visual Basic Web uygulama projesi açıldığında ve kullanıcının seçtiği bir `<td>` etiketi, geri bildirim aşağıdaki şekilde sağlanır:

- Seçimi etkin pencerede gösterilir ve yansıtılan **özellikleri** penceresi.

- Belgeye özgü **araç kutusu** etkin belgeyi yansıtacak şekilde güncelleştirilir.

- **Düzenleyicisi** araç ve **tablo** menüsü görüntülenir ve Web formu pencerenin yansıtmak için başlık çubuğunda güncelleştirir.

- Genellikle etkin olan hiyerarşi penceresinde **Çözüm Gezgini**ve geçerli bağlamı ve bağlama duyarlı yansıtmak için başlık çubuğunda güncelleştirme **proje** menü komutları, etkin Web şimdi Uygula Uygulama projesi.

## <a name="see-also"></a>Ayrıca bkz.
- [Seçim ve para birimi IDE](../../extensibility/internals/selection-and-currency-in-the-ide.md)
- [Seçim bağlamı nesneleri](../../extensibility/internals/selection-context-objects.md)
- [Hiyerarşiler ve seçim](../../extensibility/internals/hierarchies-and-selection.md)