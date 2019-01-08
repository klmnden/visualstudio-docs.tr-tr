---
title: IVariantChangeType::ChangeType | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IVariantChangeType.ChangeType
apilocation:
- scrobj.dll
helpviewer_keywords:
- IVariantChangeType::ChangeType
ms.assetid: 52374764-c42e-49af-a219-ee00c535a118
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0a02b8a3991ff6d20370cd4a2ea4cd87aa9a1226
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54086586"
---
# <a name="ivariantchangetypechangetype"></a>IVariantChangeType::ChangeType
Değişken bir değer alır ve belirtilen bir türü ile yeni bir değişken oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT ChangeType(  
   VARIANT*  pvarDst,  
   VARIANT*  pvarSrc,  
   LCID  lcid,  
   VARTYPE  vtNew  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pvarDst`  
 [out içinde] Tarafından temsil edilen değeri içeren bir değişken `pvarSrc`, ancak tarafından belirtilen tür `vtNew`.  
  
 `pvarSrc`  
 [in] Yeni bir türü değiştirmek için değişken bir değer.  
  
 `lcid`  
 [in] Bağımsız değişkenler için ya da dize dönüştürme işleminde kullanılacak yerel ayar bağlamı.  
  
 `vtNew`  
 [in] Türünü belirtir `pvarDst` olacak.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 `pvarDst` Ve `pvarSrc` bağımsız değişkenleri olabilir eşit, bu durumda, özgün değerin üzerine yazılır. Bu yöntem geçirir `pvarDst` için `VariantClear` işlevi, dolayısıyla `pvarDst` için geçerli bir değer başlatılması.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IVariantChangeType Arabirimi](../../winscript/reference/ivariantchangetype-interface.md)