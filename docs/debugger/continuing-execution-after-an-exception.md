---
title: Bir özel durum sonra yürütmeye devam | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- managed exceptions, continuing execution after
- exceptions, continuing execution after
- debugger, exceptions
- managed code, exception handling
- exception handling, continuing execution after
- execution, continuing after an exception
- program execution
- threading [Visual Studio], continuing execution after exceptions
- Exceptions dialog box
- programs, executing
ms.assetid: 6fe97aac-2131-4615-bd92-d3afee741558
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 48e0cf526d6fadcb1b91206d6e1958d89d3bdfe5
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54949975"
---
# <a name="continuing-execution-after-an-exception"></a>Özel Durumdan Sonra Yürütmeye Devam Etme
Hata ayıklayıcı bir özel durum nedeniyle yürütmeyi keserse göreceğiniz **özel durum Yardımcısı**, varsayılan olarak. Devre dışı bıraktıysanız **özel durum Yardımcısı** içinde **seçenekleri** iletişim kutusu görürsünüz **özel durum Yardımcısı'nı** (C# veya Visual Basic) veya  **Özel durum** iletişim kutusu (C++).  
  
 Zaman **özel durum Yardımcısı** görünürse, özel duruma neden olan sorunu düzeltmeye çalışın.
  
## <a name="managed-and-native-code"></a>Yönetilen ve yerel kod  
 Yönetilen ve yerel kod yürütme aynı iş parçacığında işlenmeyen bir özel durumdan sonra devam edebilirsiniz. **Özel durum Yardımcısı** burada özel durum oluşturuldu noktasına çağrı yığınını geriye doğru izler.
  
## <a name="mixed-code"></a>Karışık kod  
 Karma bir yerel ve yönetilen kod hata ayıklama sırasında işlenmeyen özel durumu, işletim sistemi kısıtlamaları çağrı yığınını geriye doğru izleme engeller. Kısayol menüsünü kullanarak çağrı yığınını geri sarma çalışırsanız, bir hata iletisi, hata ayıklayıcı işlenmeyen bir bırakma olamaz açıklar dışındaki hata ayıklama sırasında karma kodu.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özel Durumları Hata Ayıklayıcısı ile Yönetme](../debugger/managing-exceptions-with-the-debugger.md)