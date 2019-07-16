---
title: IDebugDisassemblyStream2::Seek | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugDisassemblyStream2::Seek
helpviewer_keywords:
- IDebugDisassemblyStream2::Seek
ms.assetid: afec3008-b1e0-4803-ad24-195dbfb6497e
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d774cc0bf6bca1278423249960bbc5233aa6ad37
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68203018"
---
# <a name="idebugdisassemblystream2seek"></a>IDebugDisassemblyStream2::Seek
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Ayrıştırılmış kod akış yönergeler belirtilen konuma göre verilen sayıda okuma imleci taşır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Seek(   
   SEEK_START          dwSeekStart,  
   IDebugCodeContext2* pCodeContext,  
   UINT64              uCodeLocationId,  
   INT64               iInstructions  
);  
```  
  
```csharp  
int Seek(   
   enum_SEEK_START    dwSeekStart,  
   IDebugCodeContext2 pCodeContext,  
   ulong              uCodeLocationId,  
   long               iInstructions  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `dwSeekStart`  
 [in] Bir değer [SEEK_START](../../../extensibility/debugger/reference/seek-start.md) arama işlemi başlatmak için göreceli konumun belirten sabit listesi.  
  
 `pCodeContext`  
 [in] [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) arama işlemini göreli olduğu kod bağlamı temsil eden nesne. Bu parametre yalnızca, kullanılan `dwSeekStart`  =  `SEEK_START_CODECONTEXT`; Aksi takdirde, bu parametre yoksayılır ve null değeri olabilir.  
  
 `uCodeLocationId`  
 [in] Arama işlemini göreli olduğu kod konum tanımlayıcısı. Bu parametre, kullanılan `dwSeekStart`  =  `SEEK_START_CODELOCID`; Aksi takdirde, bu parametre yoksayılır ve 0 olarak ayarlayın. İçin Açıklamalar bölümüne bakın [GetCodeLocationId](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodelocationid.md) kod konum tanımlayıcısı bir açıklaması için yöntemi.  
  
 `iInstructions`  
 [in] Belirtilen konumuna göre taşımak için yönergeler sayısını `dwSeekStart`. Bu değer, geriye için negatif olabilir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` arama konumu kullanılabilir yönergeleri listenin ötesinde bir nokta ise. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Listeye başlangıcından önce bir konumu arama ise okuma konumuna listedeki ilk yönerge ayarlanır. Bkz: listenin sonunda bir konuma ise, okuma konumuna son yönerge listesinde ayarlayın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugDisassemblyStream2](../../../extensibility/debugger/reference/idebugdisassemblystream2.md)   
 [SEEK_START](../../../extensibility/debugger/reference/seek-start.md)   
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)   
 [GetCodeLocationId](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcodelocationid.md)
