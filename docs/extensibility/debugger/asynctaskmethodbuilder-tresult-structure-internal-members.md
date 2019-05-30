---
title: AsyncTaskMethodBuilder&lt;TResult&gt; yapısı - dahili üyeler | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- AsyncTaskMethodBuilder<TResult> structure [.NET Framework debug engines]
- debug engines, AsyncTaskMethodBuilder<TResult> structure [.NET Framework]
ms.assetid: 17ebc340-8170-4aff-bf54-dc4548c83632
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c944671b3bdb42f72928822903ccb05742401f7e
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350971"
---
# <a name="asynctaskmethodbuilderlttresultgt-structure---internal-members"></a>AsyncTaskMethodBuilder&lt;TResult&gt; yapısı - dahili üyeler
Bu konu, iç üyelerini açıklar <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder%601> sınıfı. Bu sınıf hakkında genel bilgi için bkz: <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder%601> başvuru konusu.

 **Namespace:** <xref:System.Runtime.CompilerServices?displayProperty=fullName>

 **Bütünleştirilmiş kod:** mscorlib (mscorlib.dll içinde)

 Bu iç üyeleri .NET Framework'ten erişemediği için aşağıdaki söz dizimini ortak Ara dil (CIL) sağlanır.

## <a name="syntax"></a>Sözdizimi

```csharp
.class public sequential ansi sealed beforefieldinit System.Runtime.CompilerServices.AsyncTaskMethodBuilder`1<TResult>
       extends System.ValueType
       implements System.Runtime.CompilerServices.IAsyncMethodBuilder
```

## <a name="internal-members"></a>Dahili üyeler

|Ad|Açıklama|
|----------|-----------------|
|[ObjectIdForDebugger özelliği](../../extensibility/debugger/asynctaskmethodbuilder-tresult-objectidfordebugger-property.md)|Hata ayıklayıcı bu oluşturucuya benzersiz olarak tanımlanabilmesi için kullanılabilecek bir nesneyi alır.|
|[m_task alan](../../extensibility/debugger/asynctaskmethodbuilder-tresult-m-task-field.md)|Gevşek başlatılan görev yerleşik temsil eder.|

## <a name="see-also"></a>Ayrıca bkz.
- <xref:System.Runtime.CompilerServices.AsyncTaskMethodBuilder%601>
- [.NET Framework için paralel uzantı dahili bileşenleri](../../extensibility/debugger/parallel-extension-internals-for-the-dotnet-framework.md)