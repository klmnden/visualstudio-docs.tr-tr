---
title: Tümü için null denetimleri Ekle (parametreler)
ms.date: 07/24/2019
ms.topic: reference
author: stcahlon
ms.author: t-shzach
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: da3a616844dbe914cfe796ec35d1501bf83dd1ef
ms.sourcegitcommit: 3e74ec49a54e5c3da7631f4466128cdf4384af6b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "68713348"
---
# <a name="add-null-checks-for-all-parameters"></a>Tüm parametreler için null denetimleri Ekle 

Bu yeniden düzenleme için geçerlidir: 

- C# 

**Yazdırılacak** Tüm null atanabilir `if` olmayan parametrelerin null listesini denetleyen deyimler oluşturur ve ekler. 

**Oluşturulurken** Geçerli tüm Yöntem parametreleri için hızlı bir şekilde null denetimleri eklemek istiyorsunuz.

**Kaydol** Birçok parametre için null denetimleri yazmak zaman alabilir ve tekrararda olabilir. Bu yeniden düzenlemenin kullanılması hızlıdır ve programı daha sağlam hale getirir.  

## <a name="how-to"></a>Nasıl Yapılır Konuları 

1. İmlecinizi yöntemin içindeki herhangi bir parametreye yerleştirin.

2. Tuşuna **Ctrl**+ **.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

   ![Hızlı Eylemler ve yeniden düzenlemeler](media/add-null-checks-for-all-parameters.png)
   
3. **Tüm parametreler için null denetimleri ekleme**seçeneğini belirleyin.

   ![Tümü için null denetimleri Ekle](media/add-null-checks-for-all.png) 

## <a name="see-also"></a>Ayrıca bkz. 

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md) 
