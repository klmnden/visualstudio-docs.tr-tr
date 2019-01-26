---
title: IDebugFirewallConfigurationCallback2::EnsureDCOMUnblocked | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- EnsureDCOMUnblocked
- IDebugFirewallConfigurationCallback2::EnsureDCOMUnblocked
ms.assetid: acf54d27-32a6-47e7-aba6-3cc0004edc7f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 717012bec1d25263d2acebf2d5e7ea16af8e3ed7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55007691"
---
# <a name="idebugfirewallconfigurationcallback2ensuredcomunblocked"></a>IDebugFirewallConfigurationCallback2::EnsureDCOMUnblocked
Güvenlik Duvarı uzaktan hata ayıklama engellemediğinizden emin istekler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT EnsureDCOMUnblocked(   
    Void  
);  
```  
  
```csharp  
public int EnsureDCOMUnblocked();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugFirewallConfigurationCallback2](../../../extensibility/debugger/reference/idebugfirewallconfigurationcallback2.md)