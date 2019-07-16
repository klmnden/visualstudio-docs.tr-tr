---
title: IDebugProcessEx2::AddImplicitProgramNodes | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProcessEx2::AddImplicitProgramNodes
helpviewer_keywords:
- IDebugProcessEx2::AddImplicitProgramNodes method
ms.assetid: 8b491b00-f9e7-45b3-9115-fe58c3464289
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: faca728144bde572d8a1d3424fbfcf908403d679
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68202826"
---
# <a name="idebugprocessex2addimplicitprogramnodes"></a>IDebugProcessEx2::AddImplicitProgramNodes
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bu yöntem, belirtilen her hata ayıklama altyapısı (DE) için bir program düğüm ekler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT AddImplicitProgramNodes(  
   REFGUID guidLaunchingEngine,  
   GUID*   rgguidSpecificEngines,  
   DWORD   celtSpecificEngines  
);  
```  
  
```csharp  
int AddImplicitProgramNodes(  
   ref Guid guidLaunchingEngine,  
   Guid[]   rgguidSpecificEngines,  
   uint     celtSpecificEngines  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `guidLaunchingEngine`  
 [in] `GUID` , Program başlatmak için kullanılacak olan (ve kendi program düğümleri eklemek için kabul edilir) bir DE.  
  
 `rgguidSpecificEngines`  
 [in] Dizi `GUID`DEs hangi programın düğümleri eklenir, s.  
  
 `celtSpecificEngines`  
 [in] Sayısını `GUID`s'te `rgguidSpecificEngines` dizisi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 [Program düğümleri](../../../extensibility/debugger/program-nodes.md) her DE listelenen için eklenecek `rgguidSpecificEngines`— başlatma altyapısı hariç (belirtildiği `guidLaunchingEngine`), bir program başlattığında kendi program düğümü eklemek için kabul.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProgramEx2](../../../extensibility/debugger/reference/idebugprogramex2.md)   
 [Program Düğümleri](../../../extensibility/debugger/program-nodes.md)
