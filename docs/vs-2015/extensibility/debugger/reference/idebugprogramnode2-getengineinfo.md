---
title: IDebugProgramNode2::GetEngineInfo | Microsoft Docs
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
- IDebugProgramNode2::GetEngineInfo
helpviewer_keywords:
- IDebugProgramNode2::GetEngineInfo
ms.assetid: 664e7fe5-9100-4b7d-9dc5-e5a4dd0d0451
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: bdd199410c267573548077b0943107a919b2a4b9
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49283263"
---
# <a name="idebugprogramnode2getengineinfo"></a>IDebugProgramNode2::GetEngineInfo
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Ad ve tanımlayıcı bir programı çalıştırma hata ayıklama altyapısı (DE) alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT GetEngineInfo (   
   BSTR* pbstrEngine,  
   GUID* pguidEngine  
);  
```  
  
```csharp  
int GetEngineInfo(  
   out string pbstrEngine,   
   out Guid pguidEngine  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pbstrEngine`  
 [out] Programın çalıştırılması DE adını döndürür (C++ diline özgü: Bu çağrı altyapısı adını ilgilenen değil gösteren null bir işaretçi olabilir).  
  
 `pguidEngine`  
 [out] Programın çalıştırılması DE genel benzersiz tanımlayıcısını döndürür (C++ diline özgü: Bu çağırana ilişkin GUID'i altyapısının ilgilenen değil gösteren null bir işaretçi olabilir).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)

