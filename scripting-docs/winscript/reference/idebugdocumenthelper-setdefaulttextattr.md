---
title: IDebugDocumentHelper::SetDefaultTextAttr | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentHelper.SetDefaultTextAttr
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugDocumentHelper::SetDefaultTextAttr
ms.assetid: 019a4191-0019-4376-bf70-89b33e7369de
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 09f75e6f09639520462d5ef3983d67333097f76e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62948961"
---
# <a name="idebugdocumenthelpersetdefaulttextattr"></a>IDebugDocumentHelper::SetDefaultTextAttr
Bir betik bloğu içinde olmayan metin için kullanılacak varsayılan öznitelikleri ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT SetDefaultTextAttr(  
   SOURCE_TEXT_ATTR  staTextAttr  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `staTextAttr`  
 Varsayılan kaynak metin öznitelikleri.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Varsayılan öznitelikler bu yöntem tarafından değiştirmediyseniz, varsayılan öznitelikler için bir betik bloğu dışında metin SOURCETEXT_ATTR_NONSOURCE olur. Kullanıcı arabirimini, komut dosyası blokları salt okunur olarak dışında metin işaretlemek için bu bilgileri kullanabilirsiniz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugdocumenthelper arabirimi](../../winscript/reference/idebugdocumenthelper-interface.md)   
 [SOURCE_TEXT_ATTR Sabit Listesi](../../winscript/reference/source-text-attr-enumeration.md)