---
title: IDebugInterceptExceptionCompleteEvent2::GetInterceptCookie | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugInterceptExceptionCompleteEvent2::GetInterceptCookie
helpviewer_keywords:
- IDebugInterceptExceptionCompleteEvent2::GetInterceptCookie
ms.assetid: 07b20866-e598-4783-9ecc-6aa8625c8804
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: e384858fea9a7c82cf60500905f596ebe17e77bc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53893321"
---
# <a name="idebuginterceptexceptioncompleteevent2getinterceptcookie"></a>IDebugInterceptExceptionCompleteEvent2::GetInterceptCookie
Ele geçirilen bir özel durum işlemeyi tamamladığında çağrılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetInterceptCookie(  
   UINT64* pqwCookie  
);  
```  
  
```csharp  
int GetInterceptCookie(  
   out ulong pqwCookie  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pqwCookie`  
 [out] Kesildi özel durumla ilişkili benzersiz bir değerdir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Sonra [Interceptcurrentexception](../../../extensibility/debugger/reference/idebugstackframe3-interceptcurrentexception.md) yöntemi ele geçirilen bir özel durum işleme tamamlandı, gönderen [IDebugInterceptExceptionCompleteEvent2](../../../extensibility/debugger/reference/idebuginterceptexceptioncompleteevent2.md) olay. İşleyiciyi kullanabilirsiniz `GetInterceptCookie` yönteminin bir özel durumla ilişkili benzersiz bir değer almak için (geçirilen değerin `InterceptCurrentException` yöntemi).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Interceptcurrentexception](../../../extensibility/debugger/reference/idebugstackframe3-interceptcurrentexception.md)   
 [IDebugInterceptExceptionCompleteEvent2](../../../extensibility/debugger/reference/idebuginterceptexceptioncompleteevent2.md)