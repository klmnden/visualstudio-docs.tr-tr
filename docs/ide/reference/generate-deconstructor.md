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
ms.openlocfilehash: 8887f4cd6b4dcd7f08e808f1271f5d546d6a224c
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58159185"
---
# <a name="generate-a-deconstructor-in-visual-studio"></a>Visual Studio'da bir deconstructor oluşturun

Bu kod oluşturma için geçerlidir:

- C#

**Ne:** Metot taslağı için yeni bir deconstructor hemen oluşturmanıza olanak sağlar.

**ne zaman:** Düzgün türüne otomatik olarak Ayrıştır istiyorsunuz.

**Neden:** Bu özellik sizin için doğru out parametreleri ile Saplaması ancak bir deconstructor el ile yazabilirsiniz.

## <a name="generate-deconstructor"></a>Yıkıcı oluşturma

1. İstenen çıkış belirtilen parametrelerle yeni bir türü bildirin. Bu bildirim, deconstruct örneği yok, bildirim eşleştirme bulunamadığında hataya neden olur.

   ![Eksik deconstructor hatası](media/deconstruct.png)

2. Ardından, aşağıdakilerden birini yapın:

   - **Klavye**
      - Tuşuna basın, bildiriminde imlecinizi ile **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
   - **Fare**
      - Sağ tıklayıp **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
      - &nbsp; ![Tornavida](media/screwdriver.png) boş bir satıra sınıfında metin imleci ise sol kenar boşluğunda görünür simge.

      ![Deconstructor kod düzeltme](media/deconstruct-codefix.png)

3. Seçin **'MyInternalClass.Deconstruct' metodunu üret** deconstructor oluşturulacak.

   ![Sonuçta elde edilen deconstructor kod](media/deconstruct-result.png)


## <a name="see-also"></a>Ayrıca bkz.

- [Kod oluşturma](../code-generation-in-visual-studio.md)
- [Değişiklikleri Önizle](../../ide/preview-changes.md)
- [.NET Geliştiricileri için İpuçları](../../ide/visual-studio-2017-for-dotnet-developers.md)