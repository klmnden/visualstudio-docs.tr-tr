---
title: IDebugProviderProgramNode2::UnmarshalDebuggeeInterface | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
helpviewer_keywords:
- IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
ms.assetid: 2e4653c5-10f1-493c-9973-f31d266c5d48
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1af69580293e4ff37d0a23e3050955c96cc8f10b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54988278"
---
# <a name="idebugproviderprogramnode2unmarshaldebuggeeinterface"></a>IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
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
 Bu yöntem, hata ayıklama altyapısı çalışırken kullanılır [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] işlem alanına ve hata ayıklanan programa kendi işlem alanında çalışıyor.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProviderProgramNode2](../../../extensibility/debugger/reference/idebugproviderprogramnode2.md)