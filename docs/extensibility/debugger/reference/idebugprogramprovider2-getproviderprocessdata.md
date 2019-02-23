---
title: IDebugProgramProvider2::GetProviderProcessData | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramProvider2::GetProviderProcessData
helpviewer_keywords:
- IDebugProgramProvider2::GetProviderProcessData
ms.assetid: 90cf7b7f-53d2-487e-b793-94501a6e24dd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 385ef2aaaadc8d1f66eaf245f06dbfd299638fa5
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56683819"
---
# <a name="idebugprogramprovider2getproviderprocessdata"></a>IDebugProgramProvider2::GetProviderProcessData
Belirtilen bir işlemden çalışan programların listesini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetProviderProcessData(
   PROVIDER_FLAGS         Flags,
   IDebugDefaultPort2*    pPort,
   AD_PROCESS_ID          processId,
   CONST_GUID_ARRAY       EngineFilter,
   PROVIDER_PROCESS_DATA* pProcess
);
```

```csharp
int GetProviderProcessData(
   enum_PROVIDER_FLAGS     Flags,
   IDebugDefaultPort2      pPort,
   AD_PROCESS_ID           ProcessId,
   CONST_GUID_ARRAY        EngineFilter,
   PROVIDER_PROCESS_DATA[] pProcess
);
```

#### <a name="parameters"></a>Parametreler
 `Flags`

 [in] Bayraklarının bir birleşimi [PROVIDER_FLAGS](../../../extensibility/debugger/reference/provider-flags.md) sabit listesi. Bu çağrı için tipik aşağıdaki bayraklar:

|Bayrağı|Açıklama|
|----------|-----------------|
|`PFLAG_REMOTE_PORT`|Çağıran uzak makinede çalışıyor.|
|`PFLAG_DEBUGGEE`|Arayan şu anda hata ayıklaması (taşıma hakkında ek bilgi, her düğüm için de döndürülür).|
|`PFLAG_ATTACHED_TO_DEBUGGEE`|Arayan bağlı, ancak hata ayıklayıcı tarafından başlatılan değil.|
|`PFLAG_GET_PROGRAM_NODES`|Çağıran program düğümleri bir listesi için döndürülecek sorma.|

 `pPort`

 [in] Çağırma işlemi bağlantı noktası çalışıyor.

 `processId`

 [in] Bir [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md) programını içeren işlemin Kimliğini söz konusu tutan yapı.

 `EngineFilter`

 [in] Atanan (bunlar hiçbir motor belirtilirse, tüm programlar döndürülür ne sağlanan altyapılarını destekleyen üzerinde; temel, gerçekte döndürülen programların filtrelemek için kullanılacak) Bu işlemde hata ayıklamak için hata ayıklama altyapıları için GUID'leri dizisi.

 `pProcess`

 [out] A [PROVIDER_PROCESS_DATA](../../../extensibility/debugger/reference/provider-process-data.md) istenen bilgileri girilir yapısının.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, normalde bu işlemde çalışan programların listesini almak için bir işlem tarafından çağrılır. Döndürülen bilgilerin listesidir [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md) nesneleri.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProgramProvider2](../../../extensibility/debugger/reference/idebugprogramprovider2.md)
- [IDebugDefaultPort2](../../../extensibility/debugger/reference/idebugdefaultport2.md)
- [AD_PROCESS_ID](../../../extensibility/debugger/reference/ad-process-id.md)
- [CONST_GUID_ARRAY](../../../extensibility/debugger/reference/const-guid-array.md)
- [PROVIDER_FLAGS](../../../extensibility/debugger/reference/provider-flags.md)
- [PROVIDER_PROCESS_DATA](../../../extensibility/debugger/reference/provider-process-data.md)
- [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)