---
title: Kullanılmayan değerler ve parametreler
ms.date: 02/15/2019
ms.topic: reference
author: kendrahavens
ms.author: kehavens
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: 2d0875f9a298af24575cc05008713cbb6c3e2ead
ms.sourcegitcommit: 489aca71046fb6e4aafd0a4509cd7dc149d707b1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/25/2019
ms.locfileid: "58414687"
---
# <a name="unused-value-assignments-variables-and-parameters"></a>Kullanılmayan değere atamaları, değişkenler ve parametreler

Bu yeniden düzenleme için geçerlidir:

- C#
- Visual Basic

**Ne:** Belirerek kullanılmayan parametreleri ve kullanılmayan ifade değerleri için bir uyarı oluşturur. Derleyici, kullanılmayan değere atamaları bulmak için bir akış analizi de gerçekleştirir. Kullanılmayan değer atamaları Kıs ve bir ampul görünür bir [hızlı eylem](../quick-actions.md) yedekli atamasını kaldırmak için. Bilinmeyen değerleri göster ile kullanılmayan değişkenler bir [hızlı eylem](../quick-actions.md) kullanma önerisi [atar](/dotnet/csharp/discards) yerine. (Atar, uygulama kodunda kasıtlı olarak kullanılmayan geçici, işlevsiz değişkenlerdir. Bunlar bellek ayırma azaltmak ve kodunuzu daha kolay okunabilir hale getirebilirsiniz.)

**ne zaman:** Değer atamaları, parametrelerin veya hiçbir zaman kullanılmaz ifade değerleri var.

**Neden:** Bazen bir değer atama, değişken veya parametre artık kullanılıp kullanılmadığını ayırt etmek zor olabilir. Bu değerleri Soluklaşan veya bir uyarı oluşturmak, silmek hangi kodun görsel bir ipucu alın.

## <a name="unused-expression-values-and-parameters-diagnostic"></a>Kullanılmayan ifade değerleri ve parametre tanılama

1. Herhangi bir değer atama, değişken veya kullanılmayan bir parametre vardır.
2. Kullanılmayan değer atama ya da parametre soluk görünür uğradı. Kullanılmayan ifade değeri, bir uyarı oluşturur.

  ![Kullanılmayan parametre](media/unused-parameter.png)
  ![kullanılmayan değere](media/unused-value.png)
  ![kullanılmayan değer atama](media/unused-value-assignment.png)
  ![kullanılmayan değere atma](media/unused-value-discard.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [.NET Geliştiricileri için İpuçları](../../ide/visual-studio-2017-for-dotnet-developers.md)
