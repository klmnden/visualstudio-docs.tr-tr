---
title: Özel durumdan sonra sistem kodunu İnceleme | Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging, exceptions
- exceptions, debugging
ms.assetid: a38ad49b-7cf3-483d-91c4-eb3116eba50c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9b9467ce7001f0061c20a5097220bd93b24937db
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62894040"
---
# <a name="how-to-examine-system-code-after-an-exception"></a>Nasıl yapılır: Özel durumdan sonra sistem kodunu İnceleme
Bir özel durum oluştuğunda, özel durumun nedenini belirlemek için bir sistem çağrısı içinde kod İnceleme gerekebilir. Aşağıdaki yordam, sistem kodu için yüklenen semboller yoksa bunun nasıl yapılacağını ya da yalnızca kendi kodum etkin olup olmadığını açıklar.

### <a name="to-examine-system-code-following-an-exception"></a>Bir özel durumdan sonra sistem kodunu İnceleme

1. İçinde **çağrı yığını** penceresinde sağ tıklatın ve ardından tıklayın **harici kodu Göster**.

     Yalnızca kendi kodum etkin değilse, bu seçenek kısayol menüsünde kullanılabilir değil ve sistem kodunun varsayılan olarak gösterilir.

2. Artık görünen dış kod çerçeveleri sağ **çağrı yığını** penceresi.

3. İşaret **sembolleri şuradan Yükle** ve ardından **Microsoft sembol sunucuları**.

    1. Yalnızca kendi kodum etkinleştirildiğinde bir iletişim kutusu görüntülenir. Bu, yalnızca kendi kodum şimdi devre dışı olduğunu belirtir. İnto sistem çağrıları atlamak için bu gereklidir.

    2. **Ortak semboller indiriliyor** iletişim kutusu görüntülenir. Tamamlandığında indirirken kaybolur.

4. Artık Sistem kodu inceleyebilirsiniz **çağrı yığını** penceresi ve diğer windows. Örneğin, kodu bir kaynakta görmek için bir çağrı yığını çerçevesi çift tıklayabilirsiniz veya **ayrıştırılmış kodu** penceresi.

## <a name="see-also"></a>Ayrıca Bkz.
- [Özel Durumları Hata Ayıklayıcısı ile Yönetme](../debugger/managing-exceptions-with-the-debugger.md)