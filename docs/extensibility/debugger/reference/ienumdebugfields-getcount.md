---
title: IEnumDebugFields::GetCount | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IEnumDebugFields::GetCount
helpviewer_keywords:
- IEnumDebugFields::GetCount method
ms.assetid: 3f471b40-4db3-49f7-b504-58b2476eef74
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2cdbbc7f5c04436fbf98d47fea5116b63408f8b2
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54943974"
---
# <a name="ienumdebugfieldsgetcount"></a>IEnumDebugFields::GetCount
Bu yöntem numaralandırmada öğelerin sayısını döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetCount(  
   [out] ULONG* pcelt  
);  
```  
  
```csharp  
int GetCount(  
   out uint pcelt  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pcelt`  
 [out] Numaralandırmada öğelerin sayısını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem yalnızca ileri, kopyalama, atlama ve sıfırlama uygulanması gerektiğini belirten geleneksel COM numaralandırma arabiriminin bir parçası değil.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)