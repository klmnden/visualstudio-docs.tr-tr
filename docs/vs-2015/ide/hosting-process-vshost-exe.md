---
title: Barındırma süreci (vshost.exe) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- vshost.exe
- hosting process
ms.assetid: c6b9e2be-f18d-4d75-ac52-56d55784734b
caps.latest.revision: 12
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 43feac58c024c0eda8b8930fba05c0c92f7ac6bd
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65704312"
---
# <a name="hosting-process-vshostexe"></a>Barındırma Süreci (vshost.exe)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Barındırma işlemi, Visual Studio'da hata ayıklama performansını artırır, kısmi güvende hata ayıklamayı etkinleştirir ve tasarım zamanı ifade değerlendirmesi sağlayan bir özelliktir. Barındırma işlemi dosyaları, dosya adında vshost içerir ve projenizin çıkış klasörüne yerleştirilir. Daha fazla bilgi için [hata ayıklama ve barındırma işlemi](../debugger/debugging-and-the-hosting-process.md).  
  
> [!NOTE]
> İşlem dosyalarını barındıran (. vshost.exe) Visual Studio tarafından kullanılacak olan ve doğrudan çalıştırmak olmamalı veya uygulamanızla birlikte dağıtılır.  
  
## <a name="improved-debugging-performance"></a>Hata ayıklama performansı  
 Barındırma işlemi, bir uygulama etki alanı oluşturur ve hata ayıklayıcı uygulamayla ilişkilendirir. Bu görevleri gerçekleştirmek tanıtmak belirgin bir hata ayıklama zaman arasında gecikme başlatılır ve zaman uygulama çalıştırır. Barındırma işlemi uygulama etki alanı oluşturma ve hata ayıklayıcı arka planda ilişkilendirme ve uygulama etki alanı kaydetme performansı artırmak yardımcı olur ve uygulaması arasında hata ayıklayıcı durumu çalıştırır. Uygulama etki alanları hakkında daha fazla bilgi için bkz. [uygulama etki alanları](https://msdn.microsoft.com/library/113a8bbf-6875-4a72-a49d-ca2d92e19cc8).  
  
## <a name="partial-trust-debugging"></a>Kısmi güvende hata ayıklama  
 Bir uygulama içinde bir kısmi güven uygulaması olarak belirlenebilir [güvenlik sayfası](../ide/reference/security-page-project-designer.md) , **Proje Tasarımcısı**. Kısmen güvenilen uygulamada hata ayıklama, uygulama etki alanının özel başlatma gerektiriyor. Bu başlatma barındırma işlemi tarafından işlenir.  
  
## <a name="design-time-expression-evaluation"></a>Tasarım zamanı ifade değerlendirmesi  
 Tasarım zamanı ifade değerlendirmesi sağlar, kodu test etmek **hemen** uygulamayı çalıştırmak zorunda kalmadan penceresi. Barındırma işlemi, tasarım zamanı ifade değerlendirmesi sırasında bu kodu yürütür. Daha fazla bilgi için [komut penceresi](../ide/reference/immediate-window.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata ayıklama ve barındırma işlemi](../debugger/debugging-and-the-hosting-process.md)   
 [Nasıl yapılır: Barındırma işlemini devre dışı bırak](../ide/how-to-disable-the-hosting-process.md)   
 [Komut penceresi](../ide/reference/immediate-window.md)   
 [Uygulama Etki Alanları](https://msdn.microsoft.com/library/113a8bbf-6875-4a72-a49d-ca2d92e19cc8)
