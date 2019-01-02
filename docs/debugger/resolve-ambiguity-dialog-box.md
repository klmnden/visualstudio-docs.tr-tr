---
title: Belirsizliği Çöz iletişim kutusu | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.debug.Disambig
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Resolve Ambiguity dialog box
- debugger, Resolve Ambiguity dialog box
- debugging [C++], resolving ambiguity
ms.assetid: d9f47455-a116-4c84-8bad-2dfbf4d77f74
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a31d217f8dc492468a894f78f10a4f7656677521
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53945073"
---
# <a name="resolve-ambiguity-dialog-box"></a>Belirsizliği Çöz İletişim Kutusu
`Resolve Ambiguity` İletişim kutusu, hata ayıklayıcı görüntüleneceği konumun seçtiğinizde görüntülenir. Örneğin, C++ şablonları kullanıyorsanız, tek işlevi şablondan birden çok işlevler oluşturabilirsiniz. Şablonu kaynak konumda hata ayıklayıcıyı durdurur ve seçtiğiniz `Go To Disassembly`, hata ayıklayıcı birden çok seçenek vardır. Şablondan oluşturulan her işlev kendi ayrıştırılmış kodu bulunur ve hata ayıklayıcı, görüntülemek istediğiniz hangi kodun bilmez. `Resolve Ambiguity` İletişim kutusunda istediğiniz konuma karşılık gelen tüm konumlara listesinden seçmenize imkan tanır.  
  
 `Choose the specific location`  
 Komutunuz için karşılık gelen tüm konumlarda listeler.  
  
 `Address`  
 Her işlev için bellek adresleri gösterilir.  
  
 `Function`  
 Her işlevin adını gösterir.  
  
 `Module`  
 Modülü (EXE veya DLL) gösterir işlev için nesne kodu içeren.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata Ayıklayıcısındaki İfadeler](../debugger/expressions-in-the-debugger.md)