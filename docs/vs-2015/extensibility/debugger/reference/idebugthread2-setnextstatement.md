---
title: IDebugThread2::SetNextStatement | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugThread2::SetNextStatement
helpviewer_keywords:
- IDebugThread2::SetNextStatement
ms.assetid: 9e2834dd-4ecf-45af-8e6c-f9318ebdac06
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 755044ec1d713075c1c1fd3165254ba192943288
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54789443"
---
# <a name="idebugthread2setnextstatement"></a>IDebugThread2::SetNextStatement
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Verilen kod bağlamı için geçerli yönerge işaretçisini ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT SetNextStatement (   
   IDebugStackFrame2*  pStackFrame,  
   IDebugCodeContext2* pCodeContext  
);  
```  
  
```csharp  
int SetNextStatement (   
   IDebugStackFrame2  pStackFrame,  
   IDebugCodeContext2 pCodeContext  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pStackFrame`  
 Gelecekte kullanılmak üzere ayrılmış; null bir değere ayarlayın.  
  
 `pCodeContext`  
 [in] Bir [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) çalıştırılmak üzere kod konumu açıklayan nesne ve onun bağlamı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Diğer olası değerler aşağıdaki tabloda gösterilmektedir.  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|E_CANNOT_SET_NEXT_STATEMENT_ON_NONLEAF_FRAME|Sonraki deyimi çerçevenin yığın üzerinde daha derin bir yığın çerçevesinde olamaz.|  
|E_CANNOT_SETIP_TO_DIFFERENT_FUNCTION|Sonraki deyimi herhangi yığındaki çerçeveye ile ilişkili değil.|  
|E_CANNOT_SET_NEXT_STATEMENT_ON_EXCEPTION|Bazı hata ayıklama motoru özel durumdan sonra sonraki deyimi ayarlayamazsınız.|  
  
## <a name="remarks"></a>Açıklamalar  
 Yönerge işaretçisi, yürütülecek sonraki yönerge veya deyimi gösterir. Bu yöntem, bir kaynak kod satırı yeniden deneyin veya başka bir işlevde harcanan, örneğin devam etmek için yürütme zorlamak için kullanılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)
