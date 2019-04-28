---
title: IDebugProgram2::Step | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProgram2::Step
helpviewer_keywords:
- IDebugProgram2::Step
ms.assetid: e4c2ffce-9810-4088-8162-eac9ef04f2a9
caps.latest.revision: 17
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 0473cf7061cb18dad569910af5214742ba774a87
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63445784"
---
# <a name="idebugprogram2step"></a>IDebugProgram2::Step
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir adımı gerçekleştirir.  
  
> [!NOTE]
> Bu metot kullanımdan kaldırılmıştır. Kullanım [adım](../../../extensibility/debugger/reference/idebugprocess3-step.md) yöntemi yerine.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Step(   
   IDebugThread2*  pThread,  
   STEPKIND        sk,  
   STEPUNIT        step  
);  
```  
  
```csharp  
int Step(   
   IDebugThread2  pThread,  
   enum_STEPKIND  sk,  
   enum_STEPUNIT  step  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pThread`  
 [in] Bir [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) basamaklı iş parçacığını temsil eden nesne.  
  
 `sk`  
 [in] Bir değer [STEPKIND](../../../extensibility/debugger/reference/stepkind.md) adım türünü belirten sabit listesi.  
  
 `step`  
 [in] Bir değer [STEPUNIT](../../../extensibility/debugger/reference/stepunit.md) adım birimini (örneğin, ifade veya yönerge) belirten sabit listesi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Belirli bir iş parçacığının adımlanırken durumunda herhangi bir iş parçacığı eşitleme veya iş parçacıkları arasındaki iletişim, programdaki diğer iş parçacıklarını çalıştırmanız gerekir.  
  
> [!WARNING]
> Durdurma olay veya hemen (zaman uyumlu) olaya göndermeyin [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) işlenirken bu çağrı; Aksi takdirde hata ayıklayıcı kilitlenebilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugEngineProgram2](../../../extensibility/debugger/reference/idebugengineprogram2.md)   
 [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)
