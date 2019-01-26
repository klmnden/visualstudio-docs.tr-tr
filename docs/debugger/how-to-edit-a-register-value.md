---
title: 'Nasıl yapılır: YAZMAÇ değerini düzenleme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.register.edit
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- Registers window, editing register values
- register values
ms.assetid: e27b6bd8-e6d4-4f1d-8a86-9f4047bb1167
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 57ab8c2d173d5a5799d20bf50e0fd26716d163af
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54992756"
---
# <a name="how-to-edit-a-register-value-c-c-visual-basic-f"></a>Nasıl yapılır: YAZMAÇ değerini düzenleme (C#, C++, Visual Basic F#)

Yazmaçlar penceresi yalnızca adres seviyesinde hata ayıklamayı etkin değilse kullanılabilir **seçenekleri** iletişim kutusu, **hata ayıklama** düğümü.  
  
### <a name="to-change-the-value-of-a-register"></a>Bir kayıt değeri değiştirmek için  
  
1.  İçinde **kaydeder** penceresinde, SEKME tuşunu veya fare ekleme noktasını değiştirmek istediğiniz değeri için kullanın. Yazmaya başladığınızda, imleci üzerine yazmak istediğiniz değer önünde yer almalıdır.  
  
2.  Yeni bir değer girin.  
  
    > [!CAUTION]
    >  YAZMAÇ değerlerini (özellikle de EIP ve EBP kayıtları) değiştirilmesi, program yürütme etkileyebilir.  
  
    > [!CAUTION]
    >  Kayan nokta değerlerini düzenlemek, kesirli bileşenlerin ondalıktan ikiliye dönüştürülmesi nedeniyle küçük yanlışlıklara neden olabilir. Görünüşte zararsız bir düzenleme bile, kayan nokta kaydı en az önemli bitlerin bazılarının değişiklikleri neden olabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Yazmaçlar Penceresi Hakkında](../debugger/how-to-use-the-registers-window.md)