---
title: IDebugDocumentText::GetLineOfPosition | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentText.GetLineOfPosition
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugDocumentText::GetLineOfPosition
ms.assetid: fe8d4802-ea16-49ca-8973-89dcaf6c915b
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4d5d33a68b4bc87307281e37ff96f84834257a22
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62970880"
---
# <a name="idebugdocumenttextgetlineofposition"></a>IDebugDocumentText::GetLineOfPosition
Satır numarası ve isteğe bağlı olarak, karşılık gelen satır karakter kaydırma için belirli karakter konumunu döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetLineOfPosition(  
   ULONG   cCharacterPosition,  
   ULONG*  pcLineNumber,  
   ULONG*  pcCharacterOffsetInLine  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `cCharacterPosition`  
 [in] Karakter konumu aralığı konumunu başlatın.  
  
 `pcLineNumber`  
 [out] Satır numarası aralığı.  
  
 `pcCharacterOffsetInLine`  
 [out içinde] Satır aralığında karakter uzaklığı `pcLineNumber`. Bu parametre `NULL`, yöntem bir değer döndürmez.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, satır numarası ve isteğe bağlı olarak, karşılık gelen satır karakter kaydırma için belirli karakter konumunu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDocumentText Arabirimi](../../winscript/reference/idebugdocumenttext-interface.md)