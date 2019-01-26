---
title: IDebugProgramHost2::GetHostName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProgramHost2::GetHostName
helpviewer_keywords:
- IDebugProgramHost2::GetHostName
ms.assetid: 48bbb089-e59a-471a-9965-24b42a8dabf3
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 040602eeca784ac6265403f615f9234864715949
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54923275"
---
# <a name="idebugprogramhost2gethostname"></a>IDebugProgramHost2::GetHostName
Başlık, kolay ad veya bu programın barındırma işlemi dosya adını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetHostName(   
   DWORD dwType,  
   BSTR* pbstrHostName  
);  
```  
  
```csharp  
int GetHostName(   
   uint dwType,  
   out string pbstrHostName  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwType`  
 [in] Bir değer [GETHOSTNAME_TYPE](../../../extensibility/debugger/reference/gethostname-type.md) sabit listesi.  
  
 `pbstrHostName`  
 [out] Barındırma işlemi istenen adını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntemin tipik bir uygulamada `dwType` parametresi yok sayıldı ve bir kolay ad konak makinenin döndürülür. Başka bir olası uygulama geçirmektir `dwType` çağrı için parametre [GetHostName](../../../extensibility/debugger/reference/idebugprogramnode2-gethostname.md) adı almak için yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgramHost2](../../../extensibility/debugger/reference/idebugprogramhost2.md)   
 [GetHostName](../../../extensibility/debugger/reference/idebugprogramnode2-gethostname.md)