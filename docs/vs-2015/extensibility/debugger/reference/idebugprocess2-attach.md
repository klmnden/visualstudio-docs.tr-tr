---
title: IDebugProcess2::Attach | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProcess2::Attach
helpviewer_keywords:
- IDebugProcess2::Attach
ms.assetid: 40d78417-fde2-45c3-96c9-16e06bd9008d
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 4d4664f164675c445510d8976f33577684dbd1d2
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54768504"
---
# <a name="idebugprocess2attach"></a>IDebugProcess2::Attach
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Oturum hata ayıklama Yöneticisi (SDM) işlemine ekler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Attach(   
   IDebugEventCallback2* pCallback,  
   GUID*                 rgguidSpecificEngines,  
   DWORD                 celtSpecificEngines,  
   HRESULT*              rghrEngineAttach  
);  
```  
  
```csharp  
int Attach(   
   IDebugEventCallback2 pCallback,  
   Guid[]               rgguidSpecificEngines,  
   uint                 celtSpecificEngines,  
   int[]                rghrEngineAttach  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pCallback`  
 [in] Bir [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) hata ayıklama olay bildirimi için kullanılan nesne.  
  
 `rgguidSpecificEngines`  
 [in] Hata ayıklama motorlarını GUID'lerini işlemde çalışan programlarda hata ayıklama için kullanılacak bir dizi. Bu parametre null değeri olabilir. Açıklamalar, Ayrıntılar için bkz.  
  
 `celtSpecificEngines`  
 [in] Hata ayıklama sayısını altyapıları içinde `rgguidSpecificEngines` boyutu ve dizi `rghrEngineAttach` dizisi.  
  
 `rghrEngineAttach`  
 [out içinde] Hata ayıklama motoru tarafından döndürülen HRESULT kodlarını dizisi. Bu dizinin boyutu belirtilen `celtSpecificEngines` parametresi. Her kod genellikle geçerli `S_OK` veya `S_ATTACH_DEFERRED`. İkincisi DE şu anda hiçbir programlar eklendiğini gösterir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Diğer olası değerler aşağıdaki tabloda gösterilmektedir.  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`E_ATTACH_DEBUGGER_ALREADY_ATTACHED`|Belirtilen işlem için hata ayıklayıcı zaten iliştirilmiş.|  
|`E_ATTACH_DEBUGGEE_PROCESS_SECURITY_VIOLATION`|Ekleme işlemi sırasında bir güvenlik ihlali oluştu.|  
|`E_ATTACH_CANNOT_ATTACH_TO_DESKTOP`|Bir masaüstü işlemi için hata ayıklayıcı eklenemiyor.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir işlemine iliştirme ekler SDM belirtilen hata ayıklama altyapısı (DE) tarafından ayıklanabilir bu işlemde çalışan tüm programları `rgguidSpecificEngines` dizisi. Ayarlayın `rgguidSpecificEngines` parametre bir null değer veya dahil `GUID_NULL` işlemdeki tüm programlar iliştirmek için dizi.  
  
 İşlem sırasında gerçekleşen tüm hata ayıklama olayları gönderilen belirli [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) nesne. Bu `IDebugEventCallback2` SDM bu yöntemini çağırdığında nesnesi sağlanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)
