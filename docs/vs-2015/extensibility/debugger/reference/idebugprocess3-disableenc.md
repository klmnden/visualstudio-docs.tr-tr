---
title: IDebugProcess3::DisableENC | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProcess3::DisableENC
helpviewer_keywords:
- IDebugProcess3::DisableENC
ms.assetid: cffdbdac-4d76-4aeb-aa55-5d0410db99f1
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 0db9eb44b8074a5c5e3b35a5a5dadcf04f37fb2f
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63405730"
---
# <a name="idebugprocess3disableenc"></a>IDebugProcess3::DisableENC
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntemi açıkça devre dışı düzenleyin ve bu işlemi devam (ve tüm programlar içerir). Özel bağlantı noktası sağlayıcısı her zaman döndürmelidir `E_NOTIMPL`.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT DisableENC(  
   EncUnavailableReason reason  
);  
```  
  
```csharp  
   EncUnavailableReason reason  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `reason`  
 [in] Bir değer [EncUnavailableReason](../../../extensibility/debugger/reference/encunavailablereason.md) sabit listesi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.  
  
> [!NOTE]
> Özel bağlantı noktası sağlayıcısı her zaman döndürmelidir `E_NOTIMPL`.  
  
## <a name="remarks"></a>Açıklamalar  
 Düzenleme ve devam et için bir işlemi devre dışı bırakıldı, bu işlem yalnızca yeniden başlatarak yeniden etkinleştirilebilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProcess3](../../../extensibility/debugger/reference/idebugprocess3.md)   
 [EncUnavailableReason](../../../extensibility/debugger/reference/encunavailablereason.md)
