---
title: IDebugPort2::GetProcess | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPort2::GetPortSupplier
helpviewer_keywords:
- IDebugPort2::GetPortSupplier
ms.assetid: 3e2431b0-0e19-450d-8e1d-d7c314c8f872
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 64d165fedf791e26cf291ed4b6255de81873953a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62871822"
---
# <a name="idebugport2getprocess"></a>IDebugPort2::GetProcess
Bir bağlantı noktası üzerinde çalıştırılan belirtilen işlemi alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetProcess( 
   AD_PROCESS_ID    ProcessId,
   IDebugProcess2** ppProcess
);
```

```csharp
int GetProcess( 
   AD_PROCESS_ID      ProcessId,
   out IDebugProcess2 ppProcess
);
```

#### <a name="parameters"></a>Parametreler
 `ProcessId`

 [in] Bir [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md) yapı işlemi tanımlayıcısını belirtir.

 `ppProcess`

 [out] Döndürür bir [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md) işlemi temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)
- [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md)