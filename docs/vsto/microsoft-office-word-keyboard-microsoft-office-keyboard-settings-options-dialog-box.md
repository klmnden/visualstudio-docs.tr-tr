---
title: Office Word Klavyesi, Klavyesi ayarları, Seçenekler iletişim kutusu
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.ToolsOptionsPages.Microsoft_Office_Tools.Microsoft_Office_Word.Keyboard
- VS.ToolsOptionsPages.Microsoft_Office_Keyboard_Settings.Microsoft_Office_Word_Keyboard
- VST.WordOptions.KeyboardMappingScheme
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- keyboard shortcuts, Office development in Visual Studio
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 5180aa2f4c5022cedcba2c5377d2ff2ac14ffb28
ms.sourcegitcommit: cc5fd59e5dc99181601b7db8b28d7f8a83a36bab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2019
ms.locfileid: "66835987"
---
# <a name="microsoft-office-word-keyboard-microsoft-office-keyboard-settings-options-dialog-box"></a>Microsoft Office Word Klavyesi, Microsoft Office Klavyesi ayarları, Seçenekler iletişim kutusu
  Kısayol tuşları, Microsoft Office Word ve Visual Studio hem de işler. Aynı kısayol tuş bileşimi Word ve Visual Studio'da farklı komutlar için bildirimde bulunabilir. Word belge düzeyi projede Visual Studio açık olduğunda, aynı anda yalnızca bir uygulama kısayol tuşu komutlarını alır. Varsayılan olarak, Visual Studio tüm kısayol tuşu komutlarını alır, ancak Word belgesi seçerek odağa sahip olduğunda bildirim ve mesajları alacak yapabileceğiniz **dinamik klavye düzeni**.

 Şu anda kısayol tuşlarını işleyen uygulama komutuna atanmış kısayol tuşu kullanırsanız, kısayol tuşunu diğer uygulamaya geçirilir.

 Siz değiştirene kadar belirlediğiniz seçeneğe Word projeleri için yürürlükte kalır. Seçimi Microsoft Office Excel projeleri etkilemez. herhangi bir değişiklik Excel için Microsoft Office Excel Klavyesi seçenekleri kullanarak yapmalısınız.

## <a name="uielement-list"></a>UIElement listesi
 **Visual Studio klavye düzeni** Word belgesi odağa sahip olsa bile tüm kısayol tuşu komutlarını, Visual Studio alır. Örneğin, işlev tuşuna basarsanız **F5** belge odaklanmışken Visual Studio başlatılır, çözümünüzün hata ayıklama.

 **Dinamik klavye düzeni** Visual Studio, yalnızca odağı varken kısayol tuşu komutlarını alır. Word belgesi odağa sahip olduğunda, sözcük tüm kısayol tuşu komutlarını alır. Örneğin işlev tuşuna basarsanız, **F5** Word belgesi odaklanmışken Word açar **Bul ve Değiştir** iletişim kutusuyla **Git** sekmesi seçili. Basarsanız **F5** Visual Studio, Visual Studio odaklanmışken başlatır, çözümünüzün hata ayıklama.

## <a name="see-also"></a>Ayrıca bkz.
- [Microsoft Office Excel Klavyesi, Microsoft Office Klavyesi ayarları, Seçenekler iletişim kutusu](../vsto/microsoft-office-excel-keyboard-microsoft-office-keyboard-settings-options-dialog-box.md)
