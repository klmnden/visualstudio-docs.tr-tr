---
title: IA64 işlemleri için karışık mod hata ayıklaması desteklenmiyor. | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.error.interop_unsupported_ia64
dev_langs:
- CSharp
- VB
- FSharp
- C++
ms.assetid: 20bc1e38-049b-4388-87c4-936815d85b46
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 961ee6e14ea7b9f6292f14b9356e5d1ab233c8a4
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56713990"
---
# <a name="mixed-mode-debugging-for-ia64-processes-is-unsupported"></a>IA64 işlemleri için karışık mod hata ayıklaması desteklenmiyor.
Visual Studio, karma mod IA64 işlemleri yönetilen ve yerel kodda hata ayıklamayı desteklemiyor. Bu, yerel kod için yönetilen kod veya yerel koda yönetilen kod için hata ayıklama sırasında girilemiyor olduğunu anlamına gelir.

### <a name="workarounds"></a>Geçici Çözümler

-   Yönetilen ve yerel kodunuzu ayrı hata ayıklama oturumlarında hata ayıklayın.

     -veya-

     Karma kodunuzu bir 32 bitlik işlem olarak, aşağıdaki yordamlarda açıklandığı gibi hata ayıklayın.

### <a name="to-change-the-platform-to-32-bit-visual-basic-or-c"></a>Platform 32-bit (Visual Basic veya C#) değiştirileceğini

1.  İçinde **Çözüm Gezgini**, projenize sağ tıklayın ve ardından tıklayın **özellikleri** kısayol menüsünde.

2.  Özellik Sayfaları'nda tıklatın **derleme** veya **hata ayıklama** sekmesi.

3.  Tıklayın **Platform** x86 platformlar listesinden seçin.

     Varsayılan olarak, Visual Basic ve C# Derleyicileri varsayılan herhangi bir CPU üzerinde çalıştırmak için kod üretir. Bu ikili dosyalar, bir 64 bit bilgisayarda 64 bit işlem çalıştırın. Bir 32 bit işlemde çalıştırmak için seçmelisiniz **Win32**değil **AnyCPU**.

### <a name="to-change-the-platform-to-32-bit-cc"></a>32-bit (C/C++) için Platform değiştirmek için

1.  İçinde **Çözüm Gezgini**, projenize sağ tıklayın ve ardından tıklayın **özellikleri** kısayol menüsünde.

2.  Özellik Sayfaları'nda tıklatın **Platform** ve Win32 platformları listesinden seçin.

## <a name="see-also"></a>Ayrıca Bkz.
- [64 Bit Uygulamalarda Hata Ayıklama](../debugger/debug-64-bit-applications.md)