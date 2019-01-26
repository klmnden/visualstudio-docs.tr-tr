---
title: IDebugBinder3::GetAllAliases | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugBinder3::GetAllAliases
helpviewer_keywords:
- IDebugBinder3::GetAllAliases method
ms.assetid: 1f9ab2ee-2ab3-4a61-8b99-95dd7fdf3511
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e64df5e58f396462ebc9309302a7bbb7a42febcf
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55006300"
---
# <a name="idebugbinder3getallaliases"></a>IDebugBinder3::GetAllAliases
Bu yöntem programın diğer adları listesini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetAllAliases(  
   UINT          uRequest,  
   IDebugAlias** ppAliases,  
   UINT*         puFetched  
);  
```  
  
```csharp  
int GetAllAliases(  
   uint          uRequest,   
   IDebugAlias[] ppAliases,   
   out uint      puFetched  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `uRequest`  
 [in] En fazla sayısını döndürmek için diğer adlar (içine geçirilen dizinin uzunluğunu belirtir `ppAliases`).  
  
 `ppAliases`  
 [out içinde] Diğer adlar ile oturum doldurmak için dizi (Bu bir null değer ise ve `uRequest` 0 ise, döndürülen diğer adlar sayısı tarafından döndürülen `puFetched`).  
  
 `puFetched`  
 [out] Elde ettiğiniz diğer adları sayısını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugBinder3](../../../extensibility/debugger/reference/idebugbinder3.md)