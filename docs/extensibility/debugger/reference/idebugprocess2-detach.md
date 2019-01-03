---
title: IDebugProcess2::Detach | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProcess2::Detach
helpviewer_keywords:
- IDebugProcess2::Detach
ms.assetid: ee2b9084-2db1-4e49-a1d9-387284b7c3f8
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 747430b837cf682e35f5973ea35d36e72484fb3a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53988076"
---
# <a name="idebugprocess2detach"></a>IDebugProcess2::Detach
İşlemdeki tüm programları ayırıp hata ayıklayıcı bu işlemden ayırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Detach(   
   void   
);  
```  
  
```csharp  
int Detach();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Tüm programları ve işlem çalışmaya devam eder, ancak artık hata ayıklama oturumunun parçası olmayan. Ayırma işlemi bu işlemi (ve programları) için olayları gönderilecek tam, daha fazla hata ayıklama sonra.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)