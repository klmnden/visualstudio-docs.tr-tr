---
title: IDebugDocumentHelper::AddUnicodeText | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugDocumentHelper.AddUnicodeText
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugDocumentHelper::AddUnicodeText
ms.assetid: f4ef648e-c55d-4ef0-8df3-e808b798d3b8
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 391095acc1d2f541a3c497abeac5ae7248baa4e8
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63446620"
---
# <a name="idebugdocumenthelperaddunicodetext"></a>IDebugDocumentHelper::AddUnicodeText
Bir Unicode dize bu belgenin sonuna ekler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT AddUnicodeText(  
   LPCOLESTR  pszText  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pszText`  
 [in] Metni içeren null ile sonlandırılmış bir dize işaretçisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
|`E_FAIL`|Yöntem karakterleri ekleyemedi.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem oluşturur `IDebugDocumentTextEvents` bildirimleri.  
  
> [!NOTE]
> Sonra bu yöntemi çağrılırsa `AddDeferredText` çağrıldı, `E_FAIL` döndürülür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugdocumenthelper arabirimi](../../winscript/reference/idebugdocumenthelper-interface.md)   
 [IDebugDocumentHelper::AddDeferredText](../../winscript/reference/idebugdocumenthelper-adddeferredtext.md)   
 [IDebugDocumentTextEvents Arabirimi](../../winscript/reference/idebugdocumenttextevents-interface.md)