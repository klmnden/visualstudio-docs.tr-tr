---
title: 'Nasıl yapılır: özel durumdan sonra sistem kodunu İnceleme | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
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
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 91b0f0ba806868420b56f59d1b3f6de99a87886b
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49255781"
---
# <a name="how-to-examine-system-code-after-an-exception"></a>Nasıl Yapılır: Özel Durumdan Sonra Sistem Kodunu İnceleme
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





