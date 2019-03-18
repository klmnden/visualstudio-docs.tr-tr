---
title: IScriptEntry::GetSignature | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: 70cc1939ae4eb1e3c58d31b3d42b7f1b4603ce9e
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58145310"
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