---
title: IDebugPortEx2::LaunchSuspended | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugPortEx2::LaunchSuspended
helpviewer_keywords:
- IDebugPortEx2::LaunchSuspended
ms.assetid: 34b2cf99-2e52-4757-8969-1d12ac517ec0
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 3c5e57c003257650f5ca60d4a7c3d9becea3e776
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54760822"
---
# <a name="idebugportex2launchsuspended"></a>IDebugPortEx2::LaunchSuspended
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir yürütülebilir dosya başlatır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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
  
#### <a name="parameters"></a>Parametreler  
 `pszExe`  
 [in] Başlatılacak yürütülebilir dosya adı. Bu bir tam yol veya belirtilen çalışma dizini için göreli olabilir `pszDir` parametresi.  
  
 `pszArgs`  
 [in] Yürütülebilir dosyaya geçirilecek bağımsız değişkenler. Hiçbir bağımsız değişken varsa, null değeri olabilir.  
  
 `pszDir`  
 [in] Yürütülebilir dosya tarafından kullanılan çalışma dizininin adı. Çalışma dizini yok gerekiyorsa null değeri olabilir.  
  
 `bstrEnv`  
 [in] Ek bir NULL Sonlandırıcı tarafından izlenen, null ile sonlandırılmış dizeler ortam bloğu.  
  
 `hStdInput`  
 [in] Alternatif bir giriş akışına işleyin. Yeniden yönlendirme gerekmiyorsa 0 olabilir.  
  
 `hStdOutput`  
 [in] Alternatif bir çıkış akışına işleyin. Yeniden yönlendirme gerekmiyorsa 0 olabilir.  
  
 `hStdError`  
 [in] Diğer hata çıkış akışına işleyin. Yeniden yönlendirme gerekmiyorsa 0 olabilir.  
  
 `ppPortProcess`  
 [out] Döndürür bir [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md) başlatılan işlem temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, BT'nin askıya alınmış şekilde işlem ve herhangi bir kod çalıştırmayan belirmelidir. [ResumeProcess](../../../extensibility/debugger/reference/idebugportex2-resumeprocess.md) yöntemi işlemini sürdürmek için çağrılır.  
  
 Bir program bir hata ayıklama altyapısı da başlatılabilir. Ayrıntılar için bkz [Program başlatma](../../../extensibility/debugger/launching-a-program.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPortEx2](../../../extensibility/debugger/reference/idebugportex2.md)   
 [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)   
 [ResumeProcess](../../../extensibility/debugger/reference/idebugportex2-resumeprocess.md)   
 [Program Başlatma](../../../extensibility/debugger/launching-a-program.md)
