---
title: m_children alanı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- m_children field, ContingentProperties class [.NET Framework debug engines]
ms.assetid: 0a3b5653-7bc0-4a7a-8963-9020bc52b9cb
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 749b7a8da2cbdf8377e7f2e1fcb39787e2f42303
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54763607"
---
# <a name="mchildren-field"></a>m_children Alanı
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bu göreve kaydedilmiş alt görevlerin listesi.  
  
 **Namespace:** <xref:System.Threading.Tasks?displayProperty=fullName>  
  
 **Bütünleştirilmiş kod:** mscorlib (mscorlib.dll içinde)  
  
 .NET Framework'den bu iç üye erişemediği için aşağıdaki söz dizimini ortak Ara dil (CIL) sağlanır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
.field public class System.Collections.Generic.List`1<class System.Threading.Tasks.Task> m_children  
```  
  
## <a name="remarks"></a>Açıklamalar  
 Görev yürütülürken, görevi yürüten iş parçacığı bu dizinin erişmelidir.  
  
 Görev tamamlandıysa, bunlar olmayan herhangi bir şey eklemek veya herhangi bir şey kaldırın sürece diğer iş parçacıkları Bu alan erişebilirsiniz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [ContingentProperties Sınıfı](../../extensibility/debugger/contingentproperties-class-internal-members.md)
