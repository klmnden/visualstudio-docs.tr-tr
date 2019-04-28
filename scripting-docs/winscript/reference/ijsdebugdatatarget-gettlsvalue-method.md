---
title: Ijsdebugdatatarget::gettlsvalue metodu | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugDataTarget.GetTlsValue
apilocation:
- jscript9diag.dll
ms.assetid: db575be9-7b24-45c5-9008-e4f2f76d6757
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 458aaab05f274983fdaf69c6e702502974665403
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62582816"
---
# <a name="ijsdebugdatatargetgettlsvalue-method"></a>IJsDebugDataTarget::GetTlsValue Metodu
Hatası ayıklanmakta olan iş parçacığı, belirli TLS dizini için iş parçacığı yerel depolama (TLS) yuvasındaki değeri alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetTlsValue(  
   DWORD threadId,  
   UINT32 tlsIndex,  
   UINT64 *pValue  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `threadId`  
 [in] Okunacak hedef işlemde çalışan iş parçacığı.  
  
 `tlsIndex`  
 [in] Hedef işlem TlsAlloc işlevini çağırdığında, ayrılmış olan TLS dizini.  
  
 `pValue`  
 [out] İş parçacığının TLS yuvasında depolanan işaretçi boyutlu değer. Hedef iş parçacığı 32-bit ise, bu değerin üst 32-biti sıfır olacaktır.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="remarks"></a>Açıklamalar  
 Bir işlemin her bir iş parçacığı her TLS dizini için kendi yuvasına sahiptir.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebugDataTarget Arabirimi](../../winscript/reference/ijsdebugdatatarget-interface.md)