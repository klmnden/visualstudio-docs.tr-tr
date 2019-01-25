---
title: IDebugProgram2::GetProgramId | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProgram2::GetProgramId
helpviewer_keywords:
- IDebugProgram2::GetProgramId
ms.assetid: 2c31c0aa-2b71-46c7-849c-356e237d26f8
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 19c29b5cec555f9e3ad5157d7b4581777be42c98
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54756970"
---
# <a name="idebugprogram2getprogramid"></a>IDebugProgram2::GetProgramId
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu program için bir GUID alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetProgramId(   
   GUID* pguidProgramId  
);  
```  
  
```csharp  
int GetProgramId(   
   out Guid pguidProgramId  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pguidProgramId`  
 [out] Döndürür `GUID` Bu program için.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Hata ayıklama altyapısı (DE) geçirilen ilk program tanımlayıcısı döndürmelidir [OnAttach](../../../extensibility/debugger/reference/idebugprogramnodeattach2-onattach.md) veya [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) yöntemleri. Bu program kimliği arasında hata ayıklayıcı bileşenleri sağlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [OnAttach](../../../extensibility/debugger/reference/idebugprogramnodeattach2-onattach.md)   
 [Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)
