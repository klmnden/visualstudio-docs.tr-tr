---
title: Düzenle ve devam et ile kesme modunda düzenlemeleri uygulama | Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.variables.failededit
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Edit and Continue [Visual Basic], applying edits in break mode
- break mode, applying code changes
- Edit and Continue, applying edits in break mode
- editing, break mode
- coding, editing in break mode
- code, editing in break mode
ms.assetid: 1eef7498-6a1f-4fba-8146-510adc6375c9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d6c821c63354ec1b7cc83e302a3c2682982696e2
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63387683"
---
# <a name="how-to-apply-edits-in-break-mode-with-edit-and-continue-visual-basic"></a>Nasıl yapılır: Düzen ile kesme modunda düzenlemeleri uygulayın ve devam et (Visual Basic)
Düzenle ve devam et, kesme modunda kodunuzu düzenleyin ve ardından durdurup yeniden başlatmadan yürütme devam etmek için kullanabilirsiniz.

Hata ayıklarken Düzenle ve Devam Et'i kullanma ile ilgili kısıtlamalar için bkz: [desteklenen kod değişiklikleri (C# ve Visual Basic)](../debugger/supported-code-changes-csharp.md).

### <a name="to-edit-code-in-break-mode"></a>Kesme modunda kod düzenlemek için

1. Aşağıdakilerden birini yaparak Kesme moduna girin:

    - Kodunuzda bir kesme noktası ayarlayın ve ardından **hata ayıklamayı Başlat** gelen **hata ayıklama** menü ve kesme noktasına isabet uygulamaya tamamlanmasını bekleyin.

         veya

    - Hata ayıklamayı başlatın ve ardından **tümünü Kes** gelen **hata ayıklama** menüsü.

         veya

    - Bir özel durum oluştuğunda seçin **düzenlemeyi etkinleştir** üzerinde **özel durum Yardımcısı'nı**.

2. İstenen ve desteklenen kod değişiklikleri yapın.

     Daha fazla bilgi için [desteklenen kod değişiklikleri (C# ve Visual Basic)](../debugger/supported-code-changes-csharp.md).

    > [!NOTE]
    > Bir kod bu değişikliği yapmak için Düzenle ve devam et tarafından izin verilmiyor dener düzenlemeniz tarafından mor dalgalı çizgi altı çizili olacaktır ve bir görev görev listesinde görünür. Geçersiz kod değişikliği geri sürece kod yürütülmesine devam etmek mümkün olmayacaktır.

3. Üzerinde **hata ayıklama** menüsünde tıklatın **devam** yürütme devam etmek için.

     Kodunuz artık projeye dahil uygulanan düzenlemeleriniz ile yürütür.

## <a name="see-also"></a>Ayrıca Bkz.
- [Desteklenen kod değişiklikleri (C# ve Visual Basic)](../debugger/supported-code-changes-csharp.md)
- [Düzenle ve Devam Et (Visual Basic)](../debugger/edit-and-continue-visual-basic.md)
