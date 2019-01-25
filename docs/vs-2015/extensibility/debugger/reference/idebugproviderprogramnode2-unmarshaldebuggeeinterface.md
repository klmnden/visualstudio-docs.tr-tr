---
title: IDebugProviderProgramNode2::UnmarshalDebuggeeInterface | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
helpviewer_keywords:
- IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
ms.assetid: 2e4653c5-10f1-493c-9973-f31d266c5d48
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 3007d13ec3eae46511e4775497d0aad5b6325b2b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54783728"
---
# <a name="idebugproviderprogramnode2unmarshaldebuggeeinterface"></a>IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Belirtilen bir arabirim işlem sınırları alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT UnmarshalDebuggeeInterface(  
   REFIID riid,  
   void** ppvObject  
);  
```  
  
```csharp  
int UnmarshalDebuggeeInterface(  
   ref Guid   riid,  
   out IntPtr ppvObject  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `riid`  
 [in] Elde etmek için GUID arabirimi.  
  
 `ppvObject`  
 [out] İstenen arabirimini uygulayan bir nesne döndürür. [C++] Bu doğrudan istenen arabirim türüne çevirebilirsiniz. [C#] kullanın <xref:System.Runtime.InteropServices.Marshal.GetObjectForIUnknown%2A> istendiği arayüz almak için yöntemi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, hata ayıklama altyapısı çalışırken kullanılır [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)] işlem alanına ve hata ayıklanan programa kendi işlem alanında çalışıyor.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProviderProgramNode2](../../../extensibility/debugger/reference/idebugproviderprogramnode2.md)
