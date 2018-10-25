---
title: IDebugProcess3::Continue | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugProcess3::Continue
helpviewer_keywords:
- IDebugProcess3::Continue
ms.assetid: 57506242-5763-4c08-adb9-8a78ce02cebb
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f06445c53b745d26bfc2e3825cdfa4b5856c8755
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49852199"
---
# <a name="idebugprocess3continue"></a>IDebugProcess3::Continue
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu işlem durdurulmuş bir duruma çalışmaya devam eder. Herhangi bir önceki yürütme durumu (örneğin, bir adım) korunur, ve işlemi yeniden yürütmeden başlatır.  
  
> [!NOTE]
>  Bu yöntem yerine kullanılması gereken [devam](../../../extensibility/debugger/reference/idebugprogram2-continue.md).  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Continue(  
   IDebugThread2* pThread  
);  
```  
  
```csharp  
int Continue(  
   IDebugThread2 pThread  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pThread`  
 [in] Bir [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) devam etmesi gereken iş parçacığını temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, kaç işlemleri ayıklanan veya hangi işlem durdurma olay oluşturulan bağımsız olarak bu işlem çağrılır. Uygulama, önceki yürütme durumu (örneğin, bir adım) korumak ve hiçbir zaman önceki yürütme tamamlamadan önce durmuş gibi sorgulamanıza yürütmeye devam et. Diğer bir deyişle, bir iş parçacığında bu işlem bir üzerinden Adımlama ile işlemi yapmakta olduğu ve başka bir işlem durdurulduğundan durduruldu ve ardından `Continue` çağrıldı, belirtilen iş parçacığı özgün üzerinden Adımlama ile işlemi tamamlamanız gerekir.  
  
 **Uyarı** durdurma olay veya hemen (zaman uyumlu) olaya göndermeyin [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) işlenirken bu çağrı; Aksi takdirde hata ayıklayıcı kilitlenebilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProcess3](../../../extensibility/debugger/reference/idebugprocess3.md)   
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)

