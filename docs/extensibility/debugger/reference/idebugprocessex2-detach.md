---
title: IDebugProcessEx2::Detach | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProcessEx2::Detach
helpviewer_keywords:
- IDebugProcessEx2::Detach method
ms.assetid: 66d54c2c-9302-47c8-9975-f30ed988ab29
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0659dba3617e30f6d7da5ca4ebbce0c92f2e48ae
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54958007"
---
# <a name="idebugprocessex2detach"></a>IDebugProcessEx2::Detach
Bu yöntem, bir oturum işlemi artık hata ayıklıyor işlem bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Detach(   
   IDebugSession2* pSession  
);  
```  
  
```csharp  
int Detach(  
   IDebugSession2 pSession  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pSession`  
 [in] Bu işlemden ayırmak için oturum benzersiz olarak tanımlayan bir değer.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Arabirim geçirilen `pSession` oturum hata ayıklama Yöneticisi, başlangıçta benzersiz olarak tanımlayan bir değer yalnızca bir tanımlama bilgisi değerlendirilmesi için bu işleme bağlı; sağlanan arabirim yöntemleri hiçbiri işlevsel değildir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProcessEx2](../../../extensibility/debugger/reference/idebugprocessex2.md)