---
title: AsyncVoidMethodBuilder yapısı - dahili üyeler | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debug engines, AsyncVoidMethodBuilder structure [.NET Framework]
- AsyncVoidMethodBuilder structure [.NET Framework debug engines]
ms.assetid: fe2970ab-d4c5-4355-a8e4-772ee0a57178
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: d4aa6a9ab426f3773e7885b449a4b91b284cc0f2
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53875118"
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
 <xref:System.Runtime.CompilerServices.AsyncVoidMethodBuilder>   
 [.NET Framework için paralel uzantı dahili bileşenleri](../../extensibility/debugger/parallel-extension-internals-for-the-dotnet-framework.md)