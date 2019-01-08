---
title: Ijsdebug::openvirtualprocess yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJSDebug.OpenVirtualProcess
apilocation:
- jscript9diag.dll
ms.assetid: 5612bf1b-a4e3-4eaf-ac5e-c2e1f147c395
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: daa5414153ee55a431294afaf7b167ee91839bfc
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54093996"
---
# <a name="ijsdebugopenvirtualprocess-method"></a>IJsDebug::OpenVirtualProcess Yöntemi
Yeni bir sanal işlem nesnesi oluşturmak için kullanılan fabrika yöntemi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT OpenVirtualProcess(  
   DWORD processId,  
   UINT64 runtimeJsBaseAddress,  
   IJsDebugDataTarget *pDataTarget,  
   IJsDebugProcess **ppProcess  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `processId`  
 [in] Hata ayıklayıcıyı iliştirmek için işlem kimliği'ni kullanın.  
  
 `runtimeJsBaseAddress`  
 [in] Başlangıçtan JavaScript çalışma zamanı hedef işleme yüklendiği temel adres.  
  
 `pDataTarget`  
 [in] Hata ayıklayıcı, işlemin durumunu sorgulamak için sağlanan arabirim.  
  
 `ppProcess`  
 [out] Yeni hata ayıklama işlemi nesnesi  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="remarks"></a>Açıklamalar  
 Jscript9diag ve Jscript9 eşleşmiyorsa, e_jsdebug_mısmatched_runtıme döndürür.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebug Arabirimi](../../winscript/reference/ijsdebug-interface.md)