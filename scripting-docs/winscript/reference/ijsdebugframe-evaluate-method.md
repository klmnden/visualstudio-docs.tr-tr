---
title: Ijsdebugframe::evaluate yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 574af7823add67a00fc8add922b5e352fa1b369c
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54091929"
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