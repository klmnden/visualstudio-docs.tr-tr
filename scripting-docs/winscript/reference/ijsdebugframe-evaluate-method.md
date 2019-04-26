---
title: Ijsdebugframe::evaluate yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugFrame.Evaluate
apilocation:
- jscript9diag.dll
ms.assetid: 0ee61340-37b8-4fbb-a028-748b5315e279
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b328d6071ae9dc96b8e7f62bad6d4417aa1730f4
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62558196"
---
# <a name="ijsdebugframeevaluate-method"></a>IJsDebugFrame::Evaluate Yöntemi
Bu yığın çerçevesi bağlamında bir ifade değerlendirin.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT Evaluate(  
   LPCOLESTR pExpressionText,  
   IJsDebugProperty **ppDebugProperty,  
   BSTR *pError  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pExpressionText`  
 [in] Değerlendirilecek ifade.  
  
 `ppDebugProperty`  
 [out] Özellik tarayıcısını temsil eden nesne.  
  
 `pError`  
 [out] Bir hata oluşursa hata iletisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="remarks"></a>Açıklamalar  
 Aşağıdaki döndürür: S_OK: Değerlendirme başarılı, * ppDebugProperty değerlendirme sonucunu içerir. S_FALSE: Değerlendirme, bir hata atar (veya değerlendirme işlemi desteklenmiyor), \*pError hata iletisini içerir.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebugFrame Arabirimi](../../winscript/reference/ijsdebugframe-interface.md)