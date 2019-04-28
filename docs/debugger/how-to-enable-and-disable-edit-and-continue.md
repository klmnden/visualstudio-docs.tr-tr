---
title: "Nasıl yapılır: Düzenle ve Devam Et'i devre dışı bırakma ve etkinleştirme | Microsoft Docs"
ms.custom: seodec18
ms.date: 10/04/2018
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- /INCREMENTAL linker option
- Apply Code Changes command
- Edit and Continue, disabling
- code changes, applying in break mode
- INCREMENTAL linker option
- Edit and Continue, enabling
- break mode, applying code changes
- Edit and Continue, applying code changes
- Step command
- Go command
ms.assetid: fd961a1c-76fa-420d-ad8f-c1a6c003b0db
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
- cplusplus
ms.openlocfilehash: 3bee60a54576ab816c63cf60f2226ebbbaf50c44
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63388481"
---
# <a name="how-to-enable-and-disable-edit-and-continue-c-vb-c"></a>Nasıl yapılır: Düzenle ve Devam Et'i devre dışı bırakma ve etkinleştirme (C#, VB, C++)

Devre dışı bırakma veya etkinleştirme **Düzenle ve devam et** Visual Studio'daki **seçenekleri** tasarım zamanında iletişim kutusu. **Düzenle ve devam et** yalnızca hata ayıklama çalışır oluşturur. Daha fazla bilgi için [Düzenle ve devam et](../debugger/edit-and-continue.md).

Yerel c++ **Düzenle ve devam et** kullanılması `/INCREMENTAL` seçeneği. C++'ta özellik gereksinimleri hakkında daha fazla bilgi için bkz. Bu [blog gönderisi](https://devblogs.microsoft.com/cppblog/c-edit-and-continue-in-visual-studio-2015-update-3/) ve [Düzenle ve devam et (Visual C++)](../debugger/edit-and-continue-visual-cpp.md).

**Düzenle ve Devam Et'i devre dışı bırakmak veya etkinleştirmek için:**

1. Hata ayıklama oturumunda kullanıyorsanız, hata ayıklamayı Durdur (**hata ayıklama** > **hata ayıklamayı Durdur** veya **Shift**+**F5**) .

1. İçinde **Araçları** > **seçenekleri** > (veya **hata ayıklama** > **seçenekleri**) > **hataayıklama**  >  **Genel**seçin **Düzenle ve devam et** sağ bölmede.

    > [!NOTE]
    > Etkin IntelliTrace ve hem IntelliTrace olayları ve çağrı bilgilerini toplamak, Düzenle ve Devam Et'i devre dışı bırakılmıştır. Daha fazla bilgi için [IntelliTrace](../debugger/intellitrace.md).

1. C++ kodu için emin **etkinleştirme yerel Düzenle ve devam et** seçilir ve diğer seçenekleri ayarlayın:
    - **Değişiklikleri Uygula (yalnızca yerel) üzerinde devam**

      Seçili olduğunda, Visual Studio otomatik olarak derler ve kod değişikliklerini sonu durumundan hata ayıklama devam ederken geçerlidir. Aksi takdirde kullanarak değişiklikleri uygulamak seçebilirsiniz **hata ayıklama** > **kod değişikliklerini uygulama**.

    - **(Yalnızca yerel) eski kod hakkında uyar**

      Seçtiyseniz, eski kod hakkında uyarılar sağlar.

1. **Tamam**'ı tıklatın.
