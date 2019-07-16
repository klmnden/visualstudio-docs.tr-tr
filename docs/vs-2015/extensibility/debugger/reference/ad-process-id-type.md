---
title: AD_PROCESS_ID_TYPE | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- AD_PROCESS_ID_TYPE
helpviewer_keywords:
- AD_PROCESS_ID_TYPE enumeration
ms.assetid: 0aab80e9-285a-4697-94ac-c864d42a6aaa
caps.latest.revision: 7
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d471a73205383f0f23c5016872712a3ba2c578d6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68153610"
---
# <a name="adprocessidtype"></a>AD_PROCESS_ID_TYPE
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir işlem kimliği yorumlama belirtir [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md) yapısı.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
enum enum_AD_PROCESS_ID {  
   AD_PROCESS_ID_SYSTEM = 0,  
   AD_PROCESS_ID_GUID   = 1  
};  
typedef DWORD AD_PROCESS_ID_TYPE;  
```  
  
```csharp  
public enum enum_AD_PROCESS_ID {  
   AD_PROCESS_ID_SYSTEM = 0,  
   AD_PROCESS_ID_GUID   = 1  
};  
```  
  
## <a name="members"></a>Üyeler  
 AD_PROCESS_ID_SYSTEM  
 İşlem, sistem tanımlayıcısı kimliğidir. Kullanım `ProcessId.dwProcessId` alanını [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md) yapısı.  
  
 AD_PROCESS_ID_GUID  
 İşlem kimliği bir GUID değeridir. Kullanım `ProcessId.guidProcessId` alanını `AD_PROCESS_ID` yapısı.  
  
## <a name="remarks"></a>Açıklamalar  
 İçin kullanılan `ProcessIdType` üyesi [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md) yapısında bulunan işlem kimliği türünü tanımlamak için yapı. Nasıl yorumlanacağını belirler `ProcessId` bileşim yapısı içinde.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md)
