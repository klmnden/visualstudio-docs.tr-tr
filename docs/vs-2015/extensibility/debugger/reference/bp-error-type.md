---
title: BP_ERROR_TYPE | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- BP_ERROR_TYPE
helpviewer_keywords:
- BP_ERROR_TYPE enumeration
ms.assetid: c483eaab-db29-46de-bfdb-5c2a9a9cfb68
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 2317fafe410cacfca1c77b669a54669ea6e2224a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54771352"
---
# <a name="bperrortype"></a>BP_ERROR_TYPE
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir kesme noktası hata türünü belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
enum enum_BP_ERROR_TYPE {   
   BPET_NONE            = 0x00000000,  
   BPET_TYPE_WARNING    = 0x00000001,  
   BPET_TYPE_ERROR      = 0x00000002,  
   BPET_SEV_HIGH        = 0x0F000000,  
   BPET_SEV_GENERAL     = 0x07000000,  
   BPET_SEV_LOW         = 0x01000000,  
   BPET_TYPE_MASK       = 0x0000ffff,  
   BPET_SEV_MASK        = 0xffff0000,  
   BPET_GENERAL_WARNING = BPET_SEV_GENERAL | BPET_TYPE_WARNING,  
   BPET_GENERAL_ERROR   = BPET_SEV_GENERAL | BPET_TYPE_ERROR,  
   BPET_ALL             = 0xffffffff  
};  
typedef DWORD BP_ERROR_TYPE;  
```  
  
```csharp  
public enum enum_BP_ERROR_TYPE {   
   BPET_NONE            = 0x00000000,  
   BPET_TYPE_WARNING    = 0x00000001,  
   BPET_TYPE_ERROR      = 0x00000002,  
   BPET_SEV_HIGH        = 0x0F000000,  
   BPET_SEV_GENERAL     = 0x07000000,  
   BPET_SEV_LOW         = 0x01000000,  
   BPET_TYPE_MASK       = 0x0000ffff,  
   BPET_SEV_MASK        = 0xffff0000,  
   BPET_GENERAL_WARNING = BPET_SEV_GENERAL | BPET_TYPE_WARNING,  
   BPET_GENERAL_ERROR   = BPET_SEV_GENERAL | BPET_TYPE_ERROR,  
   BPET_ALL             = 0xffffffff  
};  
```  
  
## <a name="members"></a>Üyeler  
 BPET_NONE  
 Hiçbir kesme noktası hatası belirtir.  
  
 BPET_TYPE_WARNING  
 Bir uyarı stili kesme noktası hatası belirtir.  
  
 BPET_TYPE_ERROR  
 Bir hata stili kesme Notası hatası belirtir.  
  
 BPET_SEV_HIGH  
 Yüksek önem derecesi kesme noktası hatası belirtir.  
  
 BPET_SEV_GENERAL  
 Orta önem derecesi kesme noktası hatası belirtir.  
  
 BPET_SEV_LOW  
 Düşük önem derecesi kesme noktası hatası belirtir.  
  
 BPET_TYPE_MASK  
 Bir stil maskesi kesme noktası hatası belirtir.  
  
 BPET_SEV_MASK  
 Önem derecesi maskesi stili kesme noktası hatası belirtir.  
  
 BPET_GENERAL_WARNING  
 Genel uyarı stili kesme noktası hatası belirtir.  
  
 BPET_GENERAL_ERROR  
 Genel hata stili kesme noktası hatası belirtir.  
  
 BPET_ALL  
 Tüm kesme noktası hata türlerini belirtir.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu değerler, bit düzeyinde ile birleştirilebilir `OR` ve kullanılacak `dwType` üyesi [BP_ERROR_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-error-resolution-info.md) yapısı. Bir parametre olarak geçirilen [EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md) yöntemi.  
  
 Bir kesme noktası hata türü bir tür ve bir önem derecesi oluşur. Bu bir kesme noktası hata türü hiçbir zaman bir tür olduğu anlamına gelir (örneğin, `BPET_TYPE_ERROR`,) ya da bir önem derecesi (örneğin, `BPET_SEV_GENERAL`) seçemez. `BPET_GENERAL_WARNING` ve `BPET_GENERAL_ERROR` genel uyarı ve hata kesme noktaları için önceden tanımlanmış değerler sağlayın.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [BP_ERROR_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-error-resolution-info.md)   
 [EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md)
