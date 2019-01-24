---
title: IEnumDebugProcesses2::Reset | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IEnumDebugProcesses2::Reset
helpviewer_keywords:
- IEnumDebugProcesses2::Reset
ms.assetid: 31cbde4f-0bba-497a-9969-d2c342ef4a7b
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 450b469073e90b497cf2bd77e2862e48cad81b6d
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54753620"
---
# <a name="ienumdebugprocesses2reset"></a>IEnumDebugProcesses2::Reset
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Numaralandırma ilk öğeyi sıfırlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Reset(  
   void  
);  
```  
  
```csharp  
int Reset();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem çağrıldığında sonra yapılan sonraki çağrıda [sonraki](../../../extensibility/debugger/reference/ienumdebugprocesses2-next.md) yöntemi numaralandırma ilk öğeyi döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEnumDebugProcesses2](../../../extensibility/debugger/reference/ienumdebugprocesses2.md)
