---
title: Karışık modda hata ayıklama işlemleri Microsoft.NET Framework 4 kullanırken yalnızca desteklenen x64 için veya büyük | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.error.interop_unsupported_x64
dev_langs:
- CSharp
- VB
- FSharp
- C++
ms.assetid: b7495655-54c0-4315-8422-43bf63b8c22e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 821efec0beb26cea150fe0cfac20f0dc4c45d5f4
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60057816"
---
# <a name="mixed-mode-debugging-for-x64-processes-is-only-supported-when-using-microsoftnet-framework-4-or-greater"></a>x64 işlemleri için karışık modda hata ayıklama yalnızca Microsoft.NET Framework 4 veya daha yenisi kullanılırken desteklenir
.NET framework sürümleri 4 sağlamadığı'den önceki x64 karma mod hata ayıklama için destek işler. Bu, yerel kod için yönetilen kod veya yerel koda yönetilen kod için hata ayıklama sırasında girilemiyor olduğunu gösterir.

### <a name="workarounds"></a>Geçici Çözümler

- Microsoft .NET Framework 4 veya daha sonra kullanmak için projenizin güncelleştirin.

     -veya-

     Yönetilen ve yerel kodunuzu ayrı hata ayıklama oturumlarında hata ayıklayın.

     -veya-

     Karma kodunuzu bir 32 bitlik işlem olarak, aşağıdaki yordamlarda açıklandığı gibi hata ayıklayın.

### <a name="to-change-the-platform-to-32-bit-visual-basic-or-c"></a>Platform 32-bit (Visual Basic veya C#) değiştirileceğini

1. İçinde **Çözüm Gezgini**, projenize sağ tıklayın ve ardından **özellikleri**.

2. Özellik Sayfaları'nda tıklatın **derleme** veya **hata ayıklama** sekmesi.

3. Tıklayın **Platform** x86 platformlar listesinden seçin.

     Varsayılan olarak, Visual Basic ve C# Derleyicileri varsayılan herhangi bir CPU üzerinde çalıştırmak için kod üretir. Bu ikili dosyalar, bir 64 bit bilgisayarda 64 bit işlem çalıştırın. Bir 32 bit işlemde çalıştırmak için seçmelisiniz **Win32**değil **AnyCPU**.

### <a name="to-change-the-platform-to-32-bit-cc"></a>32-bit (C/C++) için platform değiştirmek için

1. İçinde **Çözüm Gezgini**, projenize sağ tıklayın ve ardından tıklayın **özellikleri**.

2. Özellik Sayfaları'nda tıklatın **Platform** ve Win32 platformları listesinden seçin.

### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

- Bkz: [SQL hata ayıklamayı kurma](/previous-versions/visualstudio/visual-studio-2010/s4sszxst(v=vs.100)).

## <a name="see-also"></a>Ayrıca Bkz.
- [64 Bit Uygulamalarda Hata Ayıklama](../debugger/debug-64-bit-applications.md)