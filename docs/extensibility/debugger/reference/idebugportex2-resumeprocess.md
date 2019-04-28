---
title: IDebugPortEx2::ResumeProcess | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortEx2::ResumeProcess
helpviewer_keywords:
- IDebugPortEx2::ResumeProcess
ms.assetid: e80a6960-9456-4764-9320-e7b1bd57fe5d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c7549ffc7375611d22e0ced603104e6a05d964b6
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62871631"
---
# <a name="idebugportex2resumeprocess"></a>IDebugPortEx2::ResumeProcess
Bir işlemin yürütülmesi devam eder.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT ResumeProcess( 
   IDebugProcess2* pPortProcess
);
```

```cpp
int ResumeProcess( 
   IDebugProcess2 pPortProcess
);
```

#### <a name="parameters"></a>Parametreler
 `pPortProcess`

 [in] Bir [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) işlemi sonlandırmaz temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugPortEx2](../../../extensibility/debugger/reference/idebugportex2.md)
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)