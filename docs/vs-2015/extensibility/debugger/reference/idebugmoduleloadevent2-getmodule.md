---
title: IDebugModuleLoadEvent2::GetModule | Microsoft Docs
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
- IDebugModuleLoadEvent2::GetModule
helpviewer_keywords:
- IDebugModuleLoadEvent2::GetModule
ms.assetid: c86482bb-9ce5-4e63-bbe0-969b50169424
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 09e1c4e0366798ae5cf10b478caa956231e08fc7
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49817632"
---
# <a name="idebugmoduleloadevent2getmodule"></a>IDebugModuleLoadEvent2::GetModule
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Yüklenmekte olan modül alır yüklü veya kaldırılmış.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetModule(   
   IDebugModule2** pModule,  
   BSTR*           pbstrDebugMessage,  
   BOOL*           pbLoad  
);  
```  
  
```csharp  
int GetModule(   
   out IDebugModule2 pModule,  
   ref string        pbstrDebugMessage,  
   ref int           pbLoad  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pModule`  
 [out] Döndürür bir [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md) yüklenmesi veya kaldırılması modülü temsil eden nesne.  
  
 `pbstrDebugMessage`  
 [out içinde] Bu olay açıklayan isteğe bağlı bir ileti döndürür. Bu parametre null değeri ise, hiçbir ileti istenir.  
  
 `pbLoad`  
 [out içinde] Sıfır olmayan (`TRUE`) Modül yükleme ve sıfır ise (`FALSE`) modülü kaldırma durumunda. Bu parametre null değeri ise, hiçbir durum istenir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugModuleLoadEvent2](../../../extensibility/debugger/reference/idebugmoduleloadevent2.md)   
 [IDebugModule2](../../../extensibility/debugger/reference/idebugmodule2.md)

