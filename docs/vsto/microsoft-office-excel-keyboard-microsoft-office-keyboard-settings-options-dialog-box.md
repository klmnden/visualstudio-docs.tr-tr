---
title: Office Excel Klavyesi, klavye ayarları, Seçenekler iletişim kutusu
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VST.ExcelOptions.KeyboardMappingScheme
- VS.ToolsOptionsPages.Microsoft_Office_Keyboard_Settings.Microsoft_Office_Excel_Keyboard
- VS.ToolsOptionsPages.Microsoft_Office_Tools.Microsoft_Office_Excel.Keyboard
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
ms.openlocfilehash: 090e943df2b61352c2342218c3c71c8f0e60eaad
ms.sourcegitcommit: cc5fd59e5dc99181601b7db8b28d7f8a83a36bab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/11/2019
ms.locfileid: "66836030"
---
# <a name="microsoft-office-excel-keyboard-microsoft-office-keyboard-settings-options-dialog-box"></a>Microsoft Office Excel Klavyesi, Microsoft Office Klavyesi ayarları, Seçenekler iletişim kutusu
  Microsoft Office Excel ve Visual Studio hem de kısayol tuşları işleyin. Aynı kısayol tuş bileşimi, Excel ve Visual Studio'da farklı komutlar için bildirimde bulunabilir. Excel belge düzeyi projede Visual Studio açık olduğunda, aynı anda yalnızca bir uygulama kısayol tuşu komutlarını alır. Varsayılan olarak, Visual Studio tüm kısayol tuşu komutlarını alır, ancak Excel belge seçerek odağa sahip olduğunda bildirim ve mesajları alacak yapabileceğiniz **dinamik klavye düzeni**.

 Şu anda kısayol tuşlarını işleyen uygulama komutuna atanmış kısayol tuşu kullanırsanız, kısayol tuşunu diğer uygulamaya geçirilir.

 Siz değiştirene kadar belirlediğiniz seçeneğe Excel projelerinde yürürlükte kalır. Seçimi Microsoft Office Word projeleri etkilemez. Microsoft Office Word Klavyesi seçeneklerini kullanarak, Word için herhangi bir değişiklik vermeniz gerekir.

## <a name="uielement-list"></a>UIElement listesi
 **Visual Studio klavye düzeni** Excel odağa sahip olsa bile tüm kısayol tuşu komutlarını, Visual Studio alır. Örneğin, işlev tuşuna basarsanız **F5** Excel odaklanmışken, Visual Studio başlatılır, çözümünüzün hata ayıklama.

 **Dinamik klavye düzeni** Visual Studio, yalnızca odağı varken kısayol tuşu komutlarını alır. Excel odağa sahip olduğunda, Excel, tüm kısayol tuşu komutlarını alır. Örneğin, işlev tuşuna basarsanız **F5** Excel odaklanmışken Excel açılır **Git** iletişim kutusu. Basarsanız **F5** Visual Studio, Visual Studio odaklanmışken başlatır, çözümünüzün hata ayıklama.

## <a name="see-also"></a>Ayrıca bkz.
- [Microsoft Office Word Klavyesi, Microsoft Office Klavyesi ayarları, Seçenekler iletişim kutusu](../vsto/microsoft-office-word-keyboard-microsoft-office-keyboard-settings-options-dialog-box.md)
