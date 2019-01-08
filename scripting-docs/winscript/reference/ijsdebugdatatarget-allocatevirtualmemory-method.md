---
title: Ijsdebugdatatarget::allocatevirtualmemory yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugDataTarget.AllocateVirtualMemory
apilocation:
- jscript9diag.dll
ms.assetid: 1d3a77b0-c1de-4a0c-a759-3e0c68fd96dd
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4eaf448e0be224f853674084a18f7aa2a6bd5ed7
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54086924"
---
# <a name="ijsdebugdatatargetallocatevirtualmemory-method"></a>IJsDebugDataTarget::AllocateVirtualMemory Yöntemi
Ayırır ve/veya hedef işlemin sanal adres alanı içindeki bellek bölgesini kaydeder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT AllocateVirtualMemory(  
   UINT64 address,  
   DWORD size,  
   DWORD allocationType,  
   DWORD pageProtection,  
   UINT64 *pAllocatedAddress  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `address`  
 [in] Burada bellek veya saklandığı hedef işlem dahilindeki adres. Bu değer genellikle hangi durumda sistem bir adres seçer, sıfırdır.  
  
 `size`  
 [in] Ayrılacak bayt cinsinden bellek bölgesini boyutu. Sistem otomatik olarak sonraki sayfa sınırına yukarı yuvarlar.  
  
 `allocationType`  
 [in] Gerçekleştirilecek ayırma türünü gösterir. Bu genellikle mem_commıt &#124; ayırır ve bir ayırmayı tek bir adımda işlemeler MEM_RESERVE (0x3000 öğesidir).  
  
 `pageProtection`  
 [in] Sayfaların ayrılacak bellek koruması bölge için. Sayfalar, bellek koruma sabitlerinden (örneğin, page_readwrıte, PAGE_EXECUTE) herhangi birini belirtebilirsiniz.  
  
 `pAllocatedAddress`  
 [out] Sayfalar ve ayrılan bölgenin taban adresidir.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="remarks"></a>Açıklamalar  
 MEM_RESET kullanılmadığı sürece, işlev sıfır olarak ayırdığı belleği başlatır. Ek bilgi için bkz. VirtualAlloc Win32 API.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebugDataTarget Arabirimi](../../winscript/reference/ijsdebugdatatarget-interface.md)