---
title: IDebugPortEx2::LaunchSuspended | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPortEx2::LaunchSuspended
helpviewer_keywords:
- IDebugPortEx2::LaunchSuspended
ms.assetid: 34b2cf99-2e52-4757-8969-1d12ac517ec0
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 94810761e546b0cae9eca32fc76bc0bfd396c7e7
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66311123"
---
# <a name="idebugportex2launchsuspended"></a>IDebugPortEx2::LaunchSuspended
Bir yürütülebilir dosya başlatır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT LaunchSuspended( 
   LPCOLESTR        pszExe,
   LPCOLESTR        pszArgs,
   LPCOLESTR        pszDir,
   BSTR             bstrEnv,
   DWORD            hStdInput,
   DWORD            hStdOutput,
   DWORD            hStdError,
   IDebugProcess2** ppPortProcess
);
```

```csharp
int LaunchSuspended( 
   string             pszExe,
   string             pszArgs,
   string             pszDir,
   string             bstrEnv,
   uint               hStdInput,
   uint               hStdOutput,
   uint               hStdError,
   out IDebugProcess2 ppPortProcess
);
```

## <a name="parameters"></a>Parametreler
`pszExe`\
[in] Başlatılacak yürütülebilir dosya adı. Bu bir tam yol veya belirtilen çalışma dizini için göreli olabilir `pszDir` parametresi.

`pszArgs`\
[in] Yürütülebilir dosyaya geçirilecek bağımsız değişkenler. Hiçbir bağımsız değişken varsa, null değeri olabilir.

`pszDir`\
[in] Yürütülebilir dosya tarafından kullanılan çalışma dizininin adı. Çalışma dizini yok gerekiyorsa null değeri olabilir.

`bstrEnv`\
[in] Ek bir NULL Sonlandırıcı tarafından izlenen, null ile sonlandırılmış dizeler ortam bloğu.

`hStdInput`\
[in] Alternatif bir giriş akışına işleyin. Yeniden yönlendirme gerekmiyorsa 0 olabilir.

`hStdOutput`\
[in] Alternatif bir çıkış akışına işleyin. Yeniden yönlendirme gerekmiyorsa 0 olabilir.

`hStdError`\
[in] Diğer hata çıkış akışına işleyin. Yeniden yönlendirme gerekmiyorsa 0 olabilir.

`ppPortProcess`\
[out] Döndürür bir [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md) başlatılan işlem temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem, BT'nin askıya alınmış şekilde işlem ve herhangi bir kod çalıştırmayan belirmelidir. [ResumeProcess](../../../extensibility/debugger/reference/idebugportex2-resumeprocess.md) yöntemi işlemini sürdürmek için çağrılır.

 Bir program bir hata ayıklama altyapısı da başlatılabilir. Ayrıntılar için bkz [Program başlatma](../../../extensibility/debugger/launching-a-program.md).

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugPortEx2](../../../extensibility/debugger/reference/idebugportex2.md)
- [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)
- [ResumeProcess](../../../extensibility/debugger/reference/idebugportex2-resumeprocess.md)
- [Program Başlatma](../../../extensibility/debugger/launching-a-program.md)