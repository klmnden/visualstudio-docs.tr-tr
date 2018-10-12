---
title: IDebugProgramPublisher2::PublishProgramNode | Microsoft Docs
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
- IDebugProgramPublisher2::PublishProgramNode
helpviewer_keywords:
- IDebugProgramPublisher2::PublishProgramNode
ms.assetid: d4b72e04-f726-46cf-8e56-5203ff205b12
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 56285933429608f766dac2ea557bb637330b1d9f
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49217704"
---
# <a name="idebugprogrampublisher2publishprogramnode"></a>IDebugProgramPublisher2::PublishProgramNode
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir program düğüm hata ayıklama Yöneticisi (SDM) hata ayıklama altyapısı (DEs) kullanımına ve oturumu için kullanılabilir hale getirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT PublishProgramNode(  
   IDebugProgramNode2 *pProgramNode  
);  
```  
  
```csharp  
int PublishProgramNode(  
   IDebugProgramNode2 pProgramNode  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pProgramNode`  
 [in] Bir [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md) kullanılabilir hale getirmek için programı düğümünü temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem seçme ve hata ayıklama için başlatmadan önce bilgi sorgulanmasını olanak verir.  
  
 Kullanılabilirlik bir program düğüm kaldırmak için çağrı [UnpublishProgramNode](../../../extensibility/debugger/reference/idebugprogrampublisher2-unpublishprogramnode.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgramPublisher2](../../../extensibility/debugger/reference/idebugprogrampublisher2.md)   
 [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)   
 [UnpublishProgramNode](../../../extensibility/debugger/reference/idebugprogrampublisher2-unpublishprogramnode.md)

