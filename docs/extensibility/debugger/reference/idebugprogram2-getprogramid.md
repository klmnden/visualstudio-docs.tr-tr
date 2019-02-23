---
title: IDebugProgram2::GetProgramId | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgram2::GetProgramId
helpviewer_keywords:
- IDebugProgram2::GetProgramId
ms.assetid: 2c31c0aa-2b71-46c7-849c-356e237d26f8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a3dfec12193efda49a520a40418b93f2d4cef6b1
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56712898"
---
# <a name="idebugprogram2getprogramid"></a>IDebugProgram2::GetProgramId
Bu program için bir GUID alır.

## <a name="syntax"></a>Sözdizimi

```cpp
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
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [OnAttach](../../../extensibility/debugger/reference/idebugprogramnodeattach2-onattach.md)
- [Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)