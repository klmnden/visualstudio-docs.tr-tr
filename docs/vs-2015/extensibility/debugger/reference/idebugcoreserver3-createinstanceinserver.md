---
title: IDebugCoreServer3::CreateInstanceInServer | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugCoreServer3::CreateInstanceInServer
helpviewer_keywords:
- IDebugCoreServer3::CreateInstanceInServer
ms.assetid: 76f36bae-f6ab-413c-a8a9-8808bfeba05b
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: f1d8964a79aaeb7b90dfbc809ec547d0282d79fa
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68205271"
---
# <a name="idebugcoreserver3createinstanceinserver"></a>IDebugCoreServer3::CreateInstanceInServer
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Sunucuda bir hata ayıklama altyapısı örneğini oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT CreateInstanceInServer(  
   LPCWSTR  szDll,  
   WORD     wLangId,  
   REFCLSID clsidObject,  
   REFIID   riid,  
   void**   ppvObject  
);  
```  
  
```csharp  
int CreateInstanceInServer(  
   string     szDll,   
   ushort     wLangID,   
   ref Guid   clsidObject,   
   ref Guid   riid,   
   out IntPtr ppvObject  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `szDll`  
 [in] Belirtilen CLSID uygulayan dll yolu `clsidObject` parametresi. Bu ise `NULL`, ardından COM's `CoCreateInstance` işlevi çağrılır.  
  
 `wLangId`  
 [in] Yerel hata ayıklama altyapısı. Bu 0 olabilir [SetLocale](../../../extensibility/debugger/reference/idebugengine2-setlocale.md) yöntemi çağırılmalıdır.  
  
 `clsidObject`  
 [in] Oluşturmak için CLSID hata ayıklama altyapısı.  
  
 `riid`  
 [in] Sınıf nesneyi almak için belirli arabirimi arabirim kimliği.  
  
 `ppvObject`  
 [out] `IUnknown` arabiriminden oluşturulan nesne. Cast veya istenen arabirim için bu nesnesi hazırlanamadı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugCoreServer3](../../../extensibility/debugger/reference/idebugcoreserver3.md)   
 [SetLocale](../../../extensibility/debugger/reference/idebugengine2-setlocale.md)
