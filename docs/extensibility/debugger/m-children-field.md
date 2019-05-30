---
title: m_children alanı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- m_children field, ContingentProperties class [.NET Framework debug engines]
ms.assetid: 0a3b5653-7bc0-4a7a-8963-9020bc52b9cb
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ab6446b18350fe1f11e0b164d9eb4bff39035ddb
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66330885"
---
# <a name="mchildren-field"></a>m_children field
Bu göreve kaydedilmiş alt görevlerin listesi.

 **Namespace:** <xref:System.Threading.Tasks?displayProperty=fullName>

 **Bütünleştirilmiş kod:** mscorlib (içinde *mscorlib.dll*)

 .NET Framework'den bu iç üye erişemediği için aşağıdaki söz dizimini ortak Ara dil (CIL) sağlanır.

## <a name="syntax"></a>Sözdizimi

```csharp
.field public class System.Collections.Generic.List`1<class System.Threading.Tasks.Task> m_children
```

## <a name="remarks"></a>Açıklamalar
 Görev yürütülürken, görevi yürüten iş parçacığı bu dizinin erişmelidir.

 Görev tamamlandıysa, diğer iş parçacıkları yoksa hiçbir şey eklemenize veya herhangi bir şey kaldırın sürece bu alan erişebilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.
- [ContingentProperties sınıfı](../../extensibility/debugger/contingentproperties-class-internal-members.md)