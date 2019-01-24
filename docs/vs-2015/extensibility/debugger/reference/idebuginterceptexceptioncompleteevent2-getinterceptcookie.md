---
title: IDebugInterceptExceptionCompleteEvent2::GetInterceptCookie | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugInterceptExceptionCompleteEvent2::GetInterceptCookie
helpviewer_keywords:
- IDebugInterceptExceptionCompleteEvent2::GetInterceptCookie
ms.assetid: 07b20866-e598-4783-9ecc-6aa8625c8804
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: e186419a102bdf48a437002ab03120587d6e0822
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54799233"
---
# <a name="idebuginterceptexceptioncompleteevent2getinterceptcookie"></a>IDebugInterceptExceptionCompleteEvent2::GetInterceptCookie
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Ele geçirilen bir özel durum işlemeyi tamamladığında çağrılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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
