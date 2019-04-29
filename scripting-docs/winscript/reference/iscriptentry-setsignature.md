---
title: IScriptEntry::SetSignature | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IScriptEntry.SetSignature
apilocation:
- scrobj.dll
helpviewer_keywords:
- IScriptEntry::SetSignature
ms.assetid: 8513587d-9df2-4621-afe7-56eacbb5e688
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 42740a0e6261317443b8c9cc23559a2f92f66540
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62787195"
---
# <a name="iscriptentrysetsignature"></a>IScriptEntry::SetSignature
Kümeleri tür bilgilerini için bir `IScriptEntry` işlev nesnesi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT SetSignature(  
   ITypeInfo          *pti  
   ULONG              iMethod  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pti`  
 [in] Tür bilgisi.  
  
 `iMethod`  
 [in] Yöntemi dizin `ITypeInfo` nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Tür bilgilerini kullanarak ayarlamak `IScriptEntry::SetSignature` veya [IScriptNode::CreateChildHandler](../../winscript/reference/iscriptnode-createchildhandler.md). Tür bilgileri, iç işlev gösterimi göre giriş tarafından da oluşturulabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IScriptEntry Arabirimi](../../winscript/reference/iscriptentry-interface.md)