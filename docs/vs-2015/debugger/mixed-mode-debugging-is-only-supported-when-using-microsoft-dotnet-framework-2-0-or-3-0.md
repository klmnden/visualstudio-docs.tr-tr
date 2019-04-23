---
title: Karışık modda hata ayıklama yalnızca Microsoft .NET Framework 2.0 veya 3.0 sürümü kullanılırken desteklenir | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.error.interop_unsupported_to_old
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: f607af6f-57fe-472a-a32e-b6202067aa96
caps.latest.revision: 8
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: e15bf0b8de7f4228fda36c1e7fda24a239f9b335
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60097381"
---
# <a name="mixed-mode-debugging-is-only-supported-when-using-microsoft-net-framework-20-or-30"></a>Karışık Modda Hata Ayıklama Yalnızca Microsoft .NET Framework 2.0 veya 3.0 Sürümü Kullanılırken Desteklenir
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Daha önce Microsoft .NET Framework sürümleri 2.0 64-bit işlemlerinin karışık mod hata ayıklama için destek sağlıyor musunuz. Bu, hata ayıklama sırasında yerel kod için yönetilen kod veya yönetilen koda yerel koddan girilemiyor anlamına gelir.  
  
 Bu sorunu gidermek için şunları yapabilirsiniz:  
  
- Microsoft .NET Framework 2.0 veya 3.0 kullanmak için projenizin güncelleştirin.  
  
- Yönetilen ve yerel kodunuzu ayrı hata ayıklama oturumlarında hata ayıklayın.  
  
- Karma kodunuzu bir 32 bitlik işlem olarak, aşağıdaki yordamlarda açıklandığı gibi hata ayıklayın.  
  
### <a name="to-change-the-operating-system-to-32-bit-visual-basic-or-c"></a>İşletim sistemi 32 bit (Visual Basic veya C#) değiştirileceğini  
  
1. İçinde **Çözüm Gezgini**, projenize sağ tıklayın ve ardından **özellikleri** kısayol menüsünde.  
  
2. Özellik Sayfaları'nda tıklatın **derleme** veya **hata ayıklama** sekmesi.  
  
3. Tıklayın **Platform**ve ardından **x86** platformlar listesinden.  
  
     Varsayılan olarak, Visual Basic ve C# Derleyicileri herhangi bir CPU üzerinde çalıştırmak için kod üretir. Bu ikili dosyalar, bir 64 bit bilgisayarda 64 bit işlem çalıştırın. Bir 32 bit işlemde çalıştırmak için seçmelisiniz **Win32**değil **AnyCPU**.  
  
### <a name="to-change-the-operating-system-to-32-bit-cc"></a>İşletim sistemi 32-bit (C/C++) değiştirileceğini  
  
1. İçinde **Çözüm Gezgini**, projenize sağ tıklayın ve ardından **özellikleri** kısayol menüsünde.  
  
     Özellik Sayfaları'nda tıklatın **Platform**ve ardından **Win32** platformlar listesinden.  
  
### <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
- Bkz: [SQL hata ayıklamayı kurma](http://msdn.microsoft.com/3db09e68-edcc-42de-9c22-4e97cfd55ab3).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [64 Bit Uygulamalarda Hata Ayıklama](../debugger/debug-64-bit-applications.md)
