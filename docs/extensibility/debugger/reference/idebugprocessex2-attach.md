---
title: IDebugProcessEx2::Attach | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProcessEx2::Attach
helpviewer_keywords:
- IDebugProcessEx2::Attach method
ms.assetid: f3334ed7-39bf-4d02-a338-36f567b9b287
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 3bef8e8016d89c2a7a4c98e9f486358fa8ba108a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53905117"
---
# <a name="idebugprocessex2attach"></a>IDebugProcessEx2::Attach
Bu yöntem, bir oturum işlemi artık hata ayıklıyor işlem bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Attach(   
   IDebugSession2* pSession  
);  
```  
  
```csharp  
int Attach(  
   IDebugSession2 pSession  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pSession`  
 [in] Bu işleme iliştirmek oturumun benzersiz olarak tanımlayan bir değer.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Arabirim geçirilen `pSession` yalnızca bir tanımlama bilgisi, bu işleme iliştirmek; oturum hata ayıklama Yöneticisi benzersiz olarak tanımlayan bir değer olarak değerlendirilmesi için sağlanan arabirim yöntemleri hiçbiri işlevsel değildir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProcessEx2](../../../extensibility/debugger/reference/idebugprocessex2.md)