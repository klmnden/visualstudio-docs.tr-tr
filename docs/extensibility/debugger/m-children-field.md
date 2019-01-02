---
title: m_children alanı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- m_children field, ContingentProperties class [.NET Framework debug engines]
ms.assetid: 0a3b5653-7bc0-4a7a-8963-9020bc52b9cb
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: a5d924e0439be2f8ab615d18a61f1303994b8dde
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53923698"
---
# <a name="mchildren-field"></a>m_children alanı
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
 [ContingentProperties sınıfı](../../extensibility/debugger/contingentproperties-class-internal-members.md)