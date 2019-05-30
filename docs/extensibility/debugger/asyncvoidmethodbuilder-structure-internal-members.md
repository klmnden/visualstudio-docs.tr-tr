---
title: AsyncVoidMethodBuilder yapısı - dahili üyeler | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debug engines, AsyncVoidMethodBuilder structure [.NET Framework]
- AsyncVoidMethodBuilder structure [.NET Framework debug engines]
ms.assetid: fe2970ab-d4c5-4355-a8e4-772ee0a57178
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 109f7d0491420ce4f3df2179dad15a582213d439
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350934"
---
# <a name="asyncvoidmethodbuilder-structure---internal-members"></a>AsyncVoidMethodBuilder yapısı - dahili üyeler
Bu konu, iç üyelerini açıklar <xref:System.Runtime.CompilerServices.AsyncVoidMethodBuilder> sınıfı. Bu sınıf hakkında genel bilgi için bkz: <xref:System.Runtime.CompilerServices.AsyncVoidMethodBuilder> başvuru konusu.

 **Namespace:** <xref:System.Runtime.CompilerServices?displayProperty=fullName>

 **Bütünleştirilmiş kod:** mscorlib (mscorlib.dll içinde)

 Bu iç üyeleri .NET Framework'ten erişemediği için aşağıdaki söz dizimini ortak Ara dil (CIL) sağlanır.

## <a name="syntax"></a>Sözdizimi

```csharp
.class public sequential ansi sealed beforefieldinit System.Runtime.CompilerServices.AsyncVoidMethodBuilder
       extends System.ValueType
       implements System.Runtime.CompilerServices.IAsyncMethodBuilder
```

## <a name="internal-members"></a>Dahili üyeler

|Ad|Açıklama|
|----------|-----------------|
|[ObjectIdForDebugger özelliği](../../extensibility/debugger/asyncvoidmethodbuilder-objectidfordebugger-property.md)|Hata ayıklayıcı bu oluşturucuya benzersiz olarak tanımlanabilmesi için kullanılabilecek bir nesneyi alır.|
|[m_objectIdForDebugger alan](../../extensibility/debugger/asyncvoidmethodbuilder-m-objectidfordebugger-field.md)|Bu oluşturucu benzersiz olarak tanımlanabilmesi için hata ayıklayıcı tarafından kullanılan gevşek başlatılan nesneyi temsil eder.|

## <a name="see-also"></a>Ayrıca bkz.
- <xref:System.Runtime.CompilerServices.AsyncVoidMethodBuilder>
- [.NET Framework için paralel uzantı dahili bileşenleri](../../extensibility/debugger/parallel-extension-internals-for-the-dotnet-framework.md)