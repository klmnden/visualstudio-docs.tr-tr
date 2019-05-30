---
title: .NET Framework için paralel uzantı dahili bileşenleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debug engines, internals [.NET Framework]
ms.assetid: 93e07cfa-91fa-464c-b866-8bf5570411df
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1ecc13be90259c68fa4d37daa5139b27b4ea8c7f
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351478"
---
# <a name="parallel-extension-internals-for-the-net-framework"></a>.NET Framework için paralel uzantı dahili bileşenleri
Bu bölümde iç türleri, yöntemleri açıklar ve .NET Framework paralel uzantılar için özel bir hata ayıklayıcı yardımcı sınıfları alanlarının uygulayın.

## <a name="in-this-section"></a>Bu bölümde
 [Görev sınıfı](../../extensibility/debugger/task-class-internal-members.md) iç veri üyelerini açıklar <xref:System.Threading.Tasks.Task?displayProperty=fullName> sınıfı.

 [TaskScheduler sınıfı](../../extensibility/debugger/taskscheduler-class-internal-members.md) iç veri üyelerini açıklar <xref:System.Threading.Tasks.TaskScheduler?displayProperty=fullName> sınıfı.

 [ContingentProperties sınıfı](../../extensibility/debugger/contingentproperties-class-internal-members.md) iç veri üyelerini açıklar `System.Threading.Tasks.ContingentProperties` sınıfı.

 [AsyncTaskMethodBuilder yapısı](../../extensibility/debugger/asynctaskmethodbuilder-structure-internal-members.md) iç üyelerini açıklar <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder> yapısı.

 [AsyncTaskMethodBuilder\<TResult > yapısı](../../extensibility/debugger/asynctaskmethodbuilder-tresult-structure-internal-members.md) iç üyelerini açıklar <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder%601> yapısı.

 [AsyncVoidMethodBuilder yapısı](../../extensibility/debugger/asyncvoidmethodbuilder-structure-internal-members.md) iç üyelerini açıklar <xref:System.Runtime.CompilerServices.AsyncVoidMethodBuilder> yapısı.

## <a name="see-also"></a>Ayrıca bkz.
- <xref:System.Threading.Tasks.Task?displayProperty=fullName>
- <xref:System.Threading.Tasks.TaskScheduler?displayProperty=fullName>
- [Visual Studio hata ayıklayıcı genişletilebilirliği](../../extensibility/debugger/visual-studio-debugger-extensibility.md)
- [Paralel Programlama](/dotnet/standard/parallel-programming/index)