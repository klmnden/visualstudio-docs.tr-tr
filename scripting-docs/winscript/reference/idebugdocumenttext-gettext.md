---
title: IDebugDocumentText::GetText | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentText.GetText
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugDocumentText::GetText
ms.assetid: 3c940a30-6c0f-4deb-aa4d-21a0bdef8461
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 63e1fee3531272f18c85c23ea83b8ca12920bd2a
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58144803"
---
# <a name="idebugdocumenttextgettext"></a>IDebugDocumentText::GetText
Karakterler ve/veya bir karakter konumu aralıkla ilişkili karakter özniteliklerini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetText(  
   ULONG              cCharacterPosition,  
   WCHAR*             pcharText,  
   SOURCE_TEXT_ATTR*  pstaTextAttr,  
   ULONG*             pcNumChars,  
   ULONG              cMaxChars  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `cCharacterPosition`  
 [in] Karakter konumu aralığı konumunu başlatın.  
  
 `pcharText`  
 [out içinde] Bir karakterin metin arabelleği. Arabellek tutabilecek kadar büyük `cMaxChars` karakter. Bu parametre NULL ise, yöntem karakterleri döndürmedi.  
  
 `pstaTextAttr`  
 [out içinde] Bir karakter özniteliğini arabelleği. Arabellek tutabilecek kadar büyük `cMaxChars` karakter. Bu parametre NULL ise, yöntem öznitelikleri döndürmez.  
  
 `pcNumChars`  
 [out içinde] Döndürülen karakter/özniteliklerinin sayısı. Bu parametre, bu yöntemi çağırmadan önce sıfır olarak ayarlanmalıdır.  
  
 `cMaxChars`  
 [in] Karakter konumu aralığı karakter sayısı. Döndürülecek karakterlerin sayısı da belirtir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, karakterleri ve/veya bir karakter konumu aralıkla ilişkili karakter özniteliklerini alır. Karakter konumu aralığı karakter konumunu bir karakter sayısı ile belirtilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugdocumenttext arabirimi](../../winscript/reference/idebugdocumenttext-interface.md)   
 [SOURCE_TEXT_ATTR Sabit Listesi](../../winscript/reference/source-text-attr-enumeration.md)