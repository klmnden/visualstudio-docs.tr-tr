---
title: Düzenle ve devam et (Visual Basic) | Microsoft Docs
ms.date: 10/11/2017
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Edit and Continue, 64-bit
- Edit and Continue [Visual Basic]
- debugging [Visual Basic], Edit and Continue
- Visual Basic, Edit and Continue
- 64-bit Edit and Continue
ms.assetid: 7e90f34f-e699-45ab-a4c9-a4b527c498c8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f73b67ac4268c04dfa9ff7ab020891623f528f9b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62851257"
---
# <a name="edit-and-continue-visual-basic"></a>Düzenle ve Devam Et (Visual Basic)
Düzenle ve devam et özelliği olan [!INCLUDE [vbprvb](../code-quality/includes/vbprvb_md.md)] , hata ayıklama kesme modunda yürütülürken kodunuzu değiştirmenize olanak sağlar. Kod düzenlemeler uygulandıktan sonra yeni düzenlemeler yerinde ile kod yürütmeyi devam etmek ve etkisine bakın.

 Düzen ve kesme moduna her özellik devam edebilirsiniz. Kesme modu, yönerge işaretçisini, kaynak penceresinde sarı bir ok, yürütülebilir bir deyimin gövdesindeki olacak bir metot veya özellik içeren satırı noktalarına sonraki yürütüldü.

 Düzenle ve devam et hata ayıklama oturumu sırasında yapmak isteyebilirsiniz değişikliklerin çoğu destekler, ancak bazı özel durumlar vardır. Daha fazla bilgi için [desteklenen kod değişiklikleri (C# ve Visual Basic)](../debugger/supported-code-changes-csharp.md).

 Yetkisiz bir düzenleme yaptığınız değişikliği mor dalgalı çizgi ile işaretlenmiş ve bir görev görev listesinde görüntülenir. Düzenle ve devam et kullanmaya devam etmek isterseniz, yetkisiz bir düzenlemeyi geri almanız gerekir. Yetkisiz olduğu belirli düzenlemeleri dış Düzenle ve devam et yapıldığında izin verilebilir. Yetkisiz bir düzenleme sonuçlarını korumak istiyorsanız, hata ayıklamayı durdurmak ve uygulamanızı yeniden başlatın.

 Düzenle ve devam et UWP uygulamaları için Windows 10 ve .NET Framework 4.6 hedefleyen x86 ve x64 uygulamaları desteklenir (yalnızca masaüstü bir sürümünde olan .NET Framework) masaüstü veya sonraki sürümleri.

 > [!NOTE]
 > Desteklenmeyen uygulamalar ve platformlar, ASP.NET 5, Silverlight 5 ve Windows 8.1 içerir.

 Düzenle ve devam et desteklenmez kullanarak hata ayıklamaya başladığınızda **iliştirme**. Düzenle ve devam et desteklenmez kod en iyileştirilmiş veya karışık yönetilen ve yerel kod. Daha fazla bilgi için [desteklenen kod değişiklikleri (C# ve Visual Basic)](../debugger/supported-code-changes-csharp.md).

 Bu bölümdeki konularda, bu özelliği kullanmak nasıl ve ne tür değişiklikler hakkında ek ayrıntılar izin verilmeyen sağlar.

## <a name="in-this-section"></a>Bu Bölümde
 [Nasıl yapılır: Düzenle ve devam et ile kesme modunda düzenlemeleri uygulama](../debugger/how-to-apply-edits-in-break-mode-with-edit-and-continue.md) kod kesme modunda düzenlemeleri uygulama açıklanmaktadır.

 [Desteklenen kod değişiklikleri (C# ve Visual Basic)](../debugger/supported-code-changes-csharp.md) ne düzenlemeleri türleri olamaz açıklar gerçekleştirilen [!INCLUDE [vb_current_short](../debugger/includes/vb_current_short_md.md)] Düzenle ve devam et.

## <a name="related-sections"></a>İlgili Bölümler
 [Düzenle ve devam et](../debugger/edit-and-continue.md) Düzenle ve devam et üzerinde konuların listesini sağlar.
