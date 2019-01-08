---
title: Ijsdebugdatatarget arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: a9b784d6-958f-4d55-b3f6-c2d6b260a16b
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e14046443ca0560deacb6ddb6e39b1fc25d18fea
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097428"
---
# <a name="ijsdebugdatatarget-interface"></a>IJsDebugDataTarget Arabirimi
Erişim ve hedef hata ayıklayıcı işleme durumunu değiştirme işlevselliği sağlamak için hata ayıklayıcı tarafından uygulanır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
IJsDebugDataTarget : public IUnknown;  
```  
  
## <a name="members"></a>Üyeler  
  
### <a name="public-methods"></a>Ortak Yöntemler  
  
|Ad|Açıklama|  
|----------|-----------------|  
|[IJsDebugDataTarget::AllocateVirtualMemory Metodu](../../winscript/reference/ijsdebugdatatarget-allocatevirtualmemory-method.md)|Ayırır ve/veya hedef işlemin sanal adres alanı içindeki bellek bölgesini kaydeder.|  
|[IJsDebugDataTarget::CreateStackFrameEnumerator Metodu](../../winscript/reference/ijsdebugdatatarget-createstackframeenumerator-method.md)|Bir yığın çerçevesi için Numaralandırıcı oluşturur.|  
|[IJsDebugDataTarget::FreeVirtualMemory Metodu](../../winscript/reference/ijsdebugdatatarget-freevirtualmemory-method.md)|Serbest bırakır ve/veya hedef işlemin sanal adres alanı içindeki bellek bölgesini kaydeder.|  
|[IJsDebugDataTarget::GetThreadContext Metodu](../../winscript/reference/ijsdebugdatatarget-getthreadcontext-method.md)|Verilen iş parçacığı için bağlamı alır.|  
|[IJsDebugDataTarget::GetTlsValue Metodu](../../winscript/reference/ijsdebugdatatarget-gettlsvalue-method.md)|Hatası ayıklanmakta olan iş parçacığı, belirli TLS dizini için iş parçacığı yerel depolama (TLS) yuvasındaki değeri alır.|  
|[IJsDebugDataTarget::ReadBSTR Metodu](../../winscript/reference/ijsdebugdatatarget-readbstr-method.md)|Hata ayıklama hedefinden bir BSTR okur.|  
|[IJsDebugDataTarget::ReadMemory Metodu](../../winscript/reference/ijsdebugdatatarget-readmemory-method.md)|Hedef işlemin belleğini okur.|  
|[IJsDebugDataTarget::ReadNullTerminatedString Metodu](../../winscript/reference/ijsdebugdatatarget-readnullterminatedstring-method.md)|Hedeften belirtilen sayıda karakteri okur.|  
|[IJsDebugDataTarget::WriteMemory Metodu](../../winscript/reference/ijsdebugdatatarget-writememory-method.md)|Hedef işlemin belleğini okur.|  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Windows Betik Arabirimleri Başvurusu](../../winscript/reference/windows-script-interfaces-reference.md)