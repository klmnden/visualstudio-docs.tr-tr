---
title: IDebugDocumentTextExternalAuthor::GetPathName | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentTextExternalAuthor.GetPathName
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugDocumentTextExternalAuthor::GetPathName
ms.assetid: 445152a1-9cf8-402e-93d6-3d4bf2b81d17
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5739e7cb0cb12661ee5683051fb7b687e62dfde4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62978760"
---
# <a name="idebugdocumenttextexternalauthorgetpathname"></a>IDebugDocumentTextExternalAuthor::GetPathName
Belgenin tam yolu ve dosya adını döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetPathName(  
   BSTR*  pbstrLongName,  
   BOOL*  pfIsOriginalFile  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pbstrLongName`  
 [out] Tam yol ve dosya adını içeren dize.  
  
 `pfIsOriginalFile`  
 [out] Yol ve dosya adı başvuruyorsa, gösteren Boole değeri için özgün belgeye.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_FAIL`|Kaynak dosya oluşturulduğunda veya belirler.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, belgenin tam yolu ve dosya adını döndürür.  
  
 Varsa `pfIsOriginalFile` FALSE, yol ve dosya adında `pbstrLongName` yeni oluşturulan geçici dosyasına bakın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocumentTextExternalAuthor Arabirimi](../../winscript/reference/idebugdocumenttextexternalauthor-interface.md)