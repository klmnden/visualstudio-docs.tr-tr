---
title: Parametre için bir yöntem hızlı Eylem Ekle
ms.date: 09/28/2018
ms.prod: visual-studio-dev15
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: da435d5bf4e0b7239b984263838c275d3b5c9ab3
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53920225"
---
# <a name="add-a-parameter-to-a-method-using-a-quick-action"></a>Hızlı bir eylem kullanarak bir yönteme bir parametre ekleyin

Bu kod oluşturma için geçerlidir:

- C#

- Visual Basic

**Ne:** Bir yöntemi kullanımınıza göre otomatik olarak bir parametre eklemenizi sağlar.

**ne zaman:** Bir yönteme parametre eklemek ve düzgün bir şekilde otomatik olarak bildirmek istiyorsanız gerekir.

**Neden:** Ancak, bu özellik üzerinde bir yöntem çağrısının dayanarak otomatik olarak ekler, çağırmadan önce yöntem bildiriminde parametre ekleyebilirsiniz.

## <a name="how-to-use-it"></a>Kullanımı

1. Ek bağımsız değişken bir yöntem çağrısını ekleyin.

   "Dalgalı" kırmızı, Çağırdığınız yöntemin adı altında görünür.

2. Hızlı Eylemler menüsü görünene kadar işaretçiyi üzerinde kırmızı "dalgalı" yerleştirin. Seçin **aşağı ok** seçin ve hızlı Eylemler menüsü **[method] için parametre Ekle**.

   ![Visual Studio'da hızlı eylem yöntemi için parametre Ekle](media/add-parameter-to-method.png)

   > [!TIP]
   > Yöntem çağrısı ve ardından ya basarak satırında imleci yerleştirerek hızlı Eylemler menüsünden erişebilirsiniz **Ctrl**+**.** ya da ampul simgesini seçerek dosya kenar boşluğunda.

   Visual Studio, yöntem bildiriminde için yeni bir parametre ekler.

> [!NOTE]
> Yöntemine yapılan diğer çağrılar varsa, bu hızlı eylem kullandıktan sonra yeni eklenen parametresi için bağımsız değişken belirtmezsiniz çünkü bunlar hataları üretebilir.

## <a name="see-also"></a>Ayrıca bkz.

- [Oluşturucusuna parametre Ekle](generate-constructor.md#addparameter)