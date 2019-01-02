---
title: IDebugProcess2::Terminate | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProcess2::Terminate
helpviewer_keywords:
- IDebugProcess2::Terminate
ms.assetid: 5e6bf373-0fe9-4321-b04a-473a65f664d9
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 5aec9bb39b23fcaea1c44855c8e146292ac0f996
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53932411"
---
# <a name="idebugprocess2terminate"></a>IDebugProcess2::Terminate
İşlemi sonlandırır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Terminate(   
   void   
);  
```  
  
```csharp  
int Terminate();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir işlem kesildiğinde tüm programlar işlem içinde sonlandırılır; yok, daha fazla kod çalışmasına izin verilmez.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)