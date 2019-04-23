---
title: 'Nasıl yapılır: YAZMAÇ değerini düzenleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.register.edit
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- VB
- CSharp
- C++
helpviewer_keywords:
- Registers window, editing register values
- register values
ms.assetid: e27b6bd8-e6d4-4f1d-8a86-9f4047bb1167
caps.latest.revision: 29
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 0ea1e932f7651439dcb9a1ff85094bd30e5239bb
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60116172"
---
# <a name="how-to-edit-a-register-value"></a>Nasıl yapılır: YAZMAÇ değerini düzenleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yazmaçlar penceresi yalnızca adres seviyesinde hata ayıklamayı etkin değilse kullanılabilir **seçenekleri** iletişim kutusu, **hata ayıklama** düğümü.  
  
### <a name="to-change-the-value-of-a-register"></a>Bir kayıt değeri değiştirmek için  
  
1. İçinde **kaydeder** penceresinde, SEKME tuşunu veya fare ekleme noktasını değiştirmek istediğiniz değeri için kullanın. Yazmaya başladığınızda, imleci üzerine yazmak istediğiniz değer önünde yer almalıdır.  
  
2. Yeni bir değer girin.  
  
    > [!CAUTION]
    >  YAZMAÇ değerlerini (özellikle de EIP ve EBP kayıtları) değiştirilmesi, program yürütme etkileyebilir.  
  
    > [!CAUTION]
    >  Kayan nokta değerlerini düzenlemek, kesirli bileşenlerin ondalıktan ikiliye dönüştürülmesi nedeniyle küçük yanlışlıklara neden olabilir. Görünüşte zararsız bir düzenleme bile, kayan nokta kaydı en az önemli bitlerin bazılarının değişiklikleri neden olabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Yazmaçlar Penceresi Hakkında](../debugger/how-to-use-the-registers-window.md)
