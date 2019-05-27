---
title: IDebugProcess2::GetAttachedSessionName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProcess2::GetAttachedSessionName
helpviewer_keywords:
- IDebugProcess2::GetAttachedSessionName
ms.assetid: 7e5e116f-2c0c-4bc8-ad3f-e9fd2318a7e4
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 84a0969eb93fc2e95449364521662c27bf6f750d
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66202651"
---
# <a name="idebugprocess2getattachedsessionname"></a>IDebugProcess2::GetAttachedSessionName
Bu işlem hata ayıklama oturumu adını alır. Bir IDE bir kullanıcı belirli bir makinenin belirli bir işlemde hata ayıklama için bu bilgileri görüntüleyebilirsiniz.

> [!NOTE]
> Bu metot kullanımdan kaldırılmıştır ve uygulaması her zaman döndürmelidir `E_NOTIMPL`.

## <a name="syntax"></a>Sözdizimi

```
HRESULT GetAttachedSessionName(
   BSTR* pbstrSessionName
);
```

## <a name="parameters"></a>Parametreler
`pbstrSessionName`\

## <a name="return-value"></a>Dönüş Değeri
 Bu yöntem her zaman döndürmelidir `E_NOTIMPL`.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)