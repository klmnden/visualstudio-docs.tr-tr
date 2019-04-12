---
title: Deconstructor hızlı Eylem oluştur
ms.date: 02/19/2019
ms.topic: reference
author: kendrahavens
ms.author: kehavens
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: f24fa988cf14bbf48fe157e2b9ee538d3eff2f35
ms.sourcegitcommit: cd91a8a4f6086cda9ba6948be25864fc7d6b8e44
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/12/2019
ms.locfileid: "59537536"
---
# <a name="generate-a-deconstructor-in-visual-studio"></a>Visual Studio'da bir deconstructor oluşturun

Bu kod oluşturma için geçerlidir:

- C#

**Ne:** Metot taslağı için yeni bir deconstructor hemen oluşturmanıza olanak sağlar.

**ne zaman:** Düzgün türüne otomatik olarak Ayrıştır istiyorsunuz.

**Neden:** Bir deconstructor el ile yazabilirsiniz, ancak bu özellik saplama sizin için doğru out parametreleri ile oluşturur.

## <a name="generate-a-deconstructor"></a>Bir deconstructor oluştur

1. İstenen çıkış belirtilen parametrelerle yeni bir türü bildirin. Bildirim eşleştirme hiçbir deconstruct örneği bulunamadığında bu bildirim hataya neden olur.

   ![Eksik deconstructor hatası](media/deconstruct.png)

2. Aşağıdaki adımlardan birini uygulayın:

   - **Klavye**
      - İmleç, bildirimi, Ctrl + seçin. Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
   - **Fare**
      - Sağ tıklayıp **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
      - Seçin ![Tornavida](media/screwdriver.png) boş bir satıra sınıfında metin imleci ise sol kenar boşluğunda görünür simge.

      ![Deconstructor kod düzeltme](media/deconstruct-codefix.png)

3. Seçin **'MyInternalClass.Deconstruct' metodunu üret** deconstructor oluşturulacak.

   ![Sonuçta elde edilen deconstructor kod](media/deconstruct-result.png)


## <a name="see-also"></a>Ayrıca bkz.

- [Kod oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizle](../../ide/preview-changes.md)
- [.NET geliştiricileri için ipuçları](../../ide/visual-studio-2017-for-dotnet-developers.md)