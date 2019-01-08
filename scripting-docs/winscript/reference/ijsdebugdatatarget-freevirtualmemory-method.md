---
title: Ijsdebugdatatarget::FreeVirtualMemory yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugDataTarget.FreeVirtualMemory
apilocation:
- jscript9diag.dll
ms.assetid: ea54bad3-9ae3-436b-974d-70fc7fffefd6
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ed5fabfca8ac9b0e9fe0dfba346b0354f4c0576f
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54086807"
---
# <a name="ijsdebugdatatargetfreevirtualmemory-method"></a>IJsDebugDataTarget::FreeVirtualMemory Yöntemi
Serbest bırakır ve/veya hedef işlemin sanal adres alanı içindeki bellek bölgesini kaydeder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT FreeVirtualMemory(  
   UINT64 address,  
   DWORD size,  
   DWORD freeType  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `address`  
 [in] Burada belleğin serbest olacağı hedef işlem adres.  
  
 `size`  
 [in] Alınacağı bayt sayısı. Bir bellek bölgesini serbest bırakmak için bu değerin sıfır olması gerekir.  
  
 `freeType`  
 [in] Gerçekleştirilecek ücretsiz işlem türünü belirtir. Genellikle, belirtilen sayfalar bölgesini serbest bırakan MEM_RELEASE (0x8000) budur. İşlemden sonra sayfalar boş durumdadır. Mem_decommıt (0x4000), bunun yerine onları bırakmadan sayfaları kaydetmek için kullanılabilir.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="remarks"></a>Açıklamalar  
 Ek bilgi için bkz. VirtualFree Win32 API.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebugDataTarget Arabirimi](../../winscript/reference/ijsdebugdatatarget-interface.md)