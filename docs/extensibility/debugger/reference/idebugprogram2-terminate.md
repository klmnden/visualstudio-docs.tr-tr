---
title: IDebugProgram2::Terminate | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgram2::Terminate
helpviewer_keywords:
- IDebugProgram2::Terminate
ms.assetid: 4d3127d3-b1e9-4b28-ac22-2f2eea255f86
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9b80afe3f0061e016301b86229f2eacedf217a43
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62870121"
---
# <a name="idebugprogram2terminate"></a>IDebugProgram2::Terminate
Program sona erer.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Terminate( 
   void 
);
```

```csharp
int Terminate();
```

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Mümkünse, program sonlandırıldı ve işlemden kaldırıldı; Aksi takdirde, hata ayıklama altyapısı (DE) gerekli tüm temizleme işlemlerini gerçekleştirir.

 Bu yöntem veya [sonlandırma](../../../extensibility/debugger/reference/idebugprocess2-terminate.md) yöntemi IDE'de, genellikle tüm hata ayıklamayı durdurma kullanıcıya yanıt tarafından çağrılır. İdeal olarak, bu yöntemin uygulanmasını program süreci içinde sonlanmalıdır. Bu mümkün değilse DE program bu işlemde daha fazla engellemeniz (ve gerekli tüm temizleme işlemlerini yapın). Varsa `IDebugProcess2::Terminate` yöntemi, IDE tarafından çağrıldı, süre sonra tüm işlem sonlandırılacak `IDebugProgram2::Terminate` yöntemi çağrılır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [Terminate](../../../extensibility/debugger/reference/idebugprocess2-terminate.md)