---
title: IDebugArrayObject2::GetBaseIndices | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- GetBaseIndices
- IDebugArrayObject2::GetBaseIndices
ms.assetid: 882951a2-3da0-49bf-8d1e-7daedd13ffe6
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 3c10fb65ec698bf9c5c9b7623b29e2f47851afe8
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54771672"
---
# <a name="idebugarrayobject2getbaseindices"></a>IDebugArrayObject2::GetBaseIndices
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Dizideki boyutların sayısı verilen her dizin için temel dizin (alt sınırı) alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetBaseIndices (  
   DWORD  dwRank,  
   DWORD* dwIndices  
);  
```  
  
```csharp  
int GetBaseIndices (  
   uint       dwRank,  
   out uint[] dwIndices  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwRank`  
 [in] Dizi boyutları (derece) sayısı.  
  
 `dwIndices`  
 [out] Dizi için temel dizin (alt sınırı).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Örneğin, bu işlev aşağıdaki C# kod tarafından oluşturulan dizi ' 5' döndürür:  
  
```  
int[] lengths = { 12 };  
int[] lowerbounds = { 5 };  
Array.CreateInstance(typeof(int), lengths, lowerbounds);  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugArrayObject2](../../../extensibility/debugger/reference/idebugarrayobject2.md)
