---
title: 'Nasıl yapılır: Özel durumdan sonra sistem kodunu İnceleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugging, exceptions
- exceptions, debugging
ms.assetid: a38ad49b-7cf3-483d-91c4-eb3116eba50c
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 289ef1825e8034566e2a9595a46919a3c498108d
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54755949"
---
# <a name="how-to-examine-system-code-after-an-exception"></a>Nasıl yapılır: Özel durumdan sonra sistem kodunu İnceleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir özel durum oluştuğunda, özel durumun nedenini belirlemek için bir sistem çağrısı içinde kod İnceleme gerekebilir. Aşağıdaki yordam, sistem kodu için yüklenen semboller yoksa bunun nasıl yapılacağını ya da yalnızca kendi kodum etkin olup olmadığını açıklar.  
  
### <a name="to-examine-system-code-following-an-exception"></a>Bir özel durumdan sonra sistem kodunu İnceleme  
  
1.  İçinde **çağrı yığını** penceresinde sağ tıklatın ve ardından tıklayın **harici kodu Göster**.  
  
     Yalnızca kendi kodum etkin değilse, bu seçenek kısayol menüsünde kullanılabilir değil ve sistem kodunun varsayılan olarak gösterilir.  
  
2.  Artık görünen dış kod çerçeveleri sağ **çağrı yığını** penceresi.  
  
3.  İşaret **sembolleri şuradan Yükle** ve ardından **Microsoft sembol sunucuları**.  
  
    1.  Yalnızca kendi kodum etkinleştirildiğinde bir iletişim kutusu görüntülenir. Bu, yalnızca kendi kodum şimdi devre dışı olduğunu belirtir. İnto sistem çağrıları atlamak için bu gereklidir.  
  
    2.  **Ortak semboller indiriliyor** iletişim kutusu görüntülenir. Tamamlandığında indirirken kaybolur.  
  
4.  Artık Sistem kodu inceleyebilirsiniz **çağrı yığını** penceresi ve diğer windows. Örneğin, kodu bir kaynakta görmek için bir çağrı yığını çerçevesi çift tıklayabilirsiniz veya **ayrıştırılmış kodu** penceresi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özel Durumları Hata Ayıklayıcısı ile Yönetme](../debugger/managing-exceptions-with-the-debugger.md)
