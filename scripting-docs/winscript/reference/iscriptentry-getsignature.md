---
title: IScriptEntry::GetSignature | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IScriptEntry.GetSignature
apilocation:
- scrobj.dll
helpviewer_keywords:
- IScriptEntry::GetSignature
ms.assetid: 8cbf37ac-b14c-4e15-a613-06f34857da9b
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 245b5806006ad94740e09e23f881e26e071a3bc1
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54092735"
---
# <a name="iscriptentrygetsignature"></a>IScriptEntry::GetSignature
Döndürür tür bilgilerini için bir `IScriptEntry` işlev nesnesi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetSignature(  
   ITypeInfo          **ppti  
   ULONG              *piMethod  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppti`  
 [out] Tür bilgilerini bununla ilişkili `IScriptEntry` işlev nesnesi.  
  
 `piMethod`  
 [out] Yöntemi dizin `ITypeInfo` nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Tür bilgilerini kullanarak ayarlamak [IScriptEntry::SetSignature](../../winscript/reference/iscriptentry-setsignature.md) veya [IScriptNode::CreateChildHandler](../../winscript/reference/iscriptnode-createchildhandler.md). Tür bilgileri, iç işlev gösterimi göre giriş tarafından da oluşturulabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IScriptEntry Arabirimi](../../winscript/reference/iscriptentry-interface.md)