---
title: 'Ihata ayıklama Garrayobject:: GetDimensions | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugArrayObject::GetDimensions
helpviewer_keywords:
- IDebugArrayObject::GetDimensions method
ms.assetid: 113e0aff-9028-49d6-b104-9fe7be4772d7
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 09902c60f87cfb92d0f0778fcbd106ade4d8dac4
ms.sourcegitcommit: 9cfd3ef6c65f671a26322320818212a1ed5955fe
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/26/2019
ms.locfileid: "68197784"
---
# <a name="idebugarrayobjectgetdimensions"></a>IDebugArrayObject::GetDimensions
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Dizinin boyutlarını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetDimensions(   
   DWORD dwCount,  
   DWORD dwDimensions[]  
);  
```  
  
```csharp  
int GetDimensions(  
   [In] uint    dwCount,   
   [Out] uint[] dwDimensions  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwCount`  
 'ndaki Alınacak boyut sayısı.  
  
 `dwDimensions`  
 [in, out] Her boyutun boyutlarıyla doldurulmuş bir dizi. `dwCount``dwDimensions` dizinin en büyük boyutunu belirtir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa, S_OK döndürür; Aksi takdirde, bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Çok boyutlu bir dizi, her boyut için farklı boyutlarda olabilir. Örneğin, üç boyutlu dizi `myarray[3][2][6]`verildiğinde, bu yöntem bu sırada `dwDimensions` parametreye 3, 2 ve 6 döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugArrayObject](../../../extensibility/debugger/reference/idebugarrayobject.md)
