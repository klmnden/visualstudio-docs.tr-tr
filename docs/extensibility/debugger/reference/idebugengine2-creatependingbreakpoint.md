---
title: IDebugEngine2::CreatePendingBreakpoint | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngine2::CreatePendingBreakpoint
helpviewer_keywords:
- IDebugEngine2::CreatePendingBreakpoint
ms.assetid: 92e85b90-a931-48d9-89a7-a6edcb83ae5a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 72719a2dc6d424487c0fdd6b5850ff7f1d1e29aa
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56703389"
---
# <a name="idebugengine2creatependingbreakpoint"></a>IDebugEngine2::CreatePendingBreakpoint
Hata ayıklama altyapısı (DE) bir bekleyen kesme noktası oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT CreatePendingBreakpoint(
    IDebugBreakpointRequest2*  pBPRequest,
    IDebugPendingBreakpoint2** ppPendingBP
);
```

```csharp
int CreatePendingBreakpoint(
    IDebugBreakpointRequest2     pBPRequest,
    out IDebugPendingBreakpoint2 ppPendingBP
);
```

#### <a name="parameters"></a>Parametreler
`pBPRequest`

 [in] Bir [IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md) oluşturmak için bekleyen kesme noktasını tanımlayan nesne.

`ppPendingBP`

 [out] Döndürür bir [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md) bekleyen kesme noktasının temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Genellikle döndürür `E_FAIL` varsa `pBPRequest` parametresi biri DE tarafından desteklenen herhangi bir dilde eşleşmiyor `pBPRequest` parametresi, geçersiz veya eksik.

## <a name="remarks"></a>Açıklamalar
Bir bekleyen kesme noktasının aslında bir kesme noktası kodunu bağlamak için gerekli tüm bilgileri bir koleksiyonudur. Bu yöntemin döndürdüğü bekleyen kesme noktasına kadar koduna bağlı değil [bağlama](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md) yöntemi çağrılır.

Bekleyen kesme noktası her kullanıcı kümeleri oturum hata ayıklama Yöneticisi (SDM) her ekli DE bu yöntemi çağırır. Bu kesme noktası o DE içinde çalışan programlar için geçerli olduğunu doğrulamak için DE en fazla olur.

Kullanıcı, bir kod satırında bir kesme noktası ayarlar, bu koda karşılık gelen belgedeki en yakın satır kesme noktasını bağlamak DE ücretsizdir. Bu kullanıcının çok satırlı deyiminin ilk satırında bir kesme noktası ayarlayın, ancak son satırda (burada tüm kodlar hata ayıklama bilgilerini öznitelendirilen) bağlamak mümkün kılar.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu yöntem için basit bir uygulama gösterilmektedir `CProgram` nesne. DE'ın uygulaması `IDebugEngine2::CreatePendingBreakpoint` sonra bu uygulama, her programda yöntemin tüm çağrıları iletebilir.

```
HRESULT CProgram::CreatePendingBreakpoint(IDebugBreakpointRequest2* pBPRequest, IDebugPendingBreakpoint2** ppPendingBP)
{
    // Create and initialize the CPendingBreakpoint object.
    CComObject<CPendingBreakpoint> *pPending;
    CComObject<CPendingBreakpoint>::CreateInstance(&pPending);
    pPending->Initialize(pBPRequest, m_pInterp, m_pCallback, m_pEngine);
    return pPending->QueryInterface(ppPendingBP);
}
```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)
- [Bind](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md)
- [IDebugBreakpointRequest2](../../../extensibility/debugger/reference/idebugbreakpointrequest2.md)
- [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)
