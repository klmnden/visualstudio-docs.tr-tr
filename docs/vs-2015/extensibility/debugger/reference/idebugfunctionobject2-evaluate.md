---
title: IDebugFunctionObject2::Evaluate | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- IDebugFunctionObject2::Evaluate
ms.assetid: bc54c652-904b-4297-a6db-faa329684881
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 2637d75af31b03a29e63dd8b68c4e3c75256b520
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49259139"
---
# <a name="idebugfunctionobject2evaluate"></a>IDebugFunctionObject2::Evaluate
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

İşlevini çağırır ve bir nesne olarak elde edilen değeri döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Evaluate (  
   IDebugObject** ppParams,  
   DWORD          dwParams,  
   DWORD          dwEvalFlags,  
   DWORD          dwTimeout,  
   IDebugObject** ppResult  
);  
```  
  
```csharp  
int Evaluate (  
   IDebugObject     ppParams,  
   uint             dwParams,  
   uint             dwEvalFlags,  
   uint             dwTimeout,  
   out IDebugObject ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppParams`  
 [in] Bir dizi [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) giriş parametrelerini temsil eden nesneleri. Bu parametrelerin her biri, bu arabirimde Oluştur yöntemlerden birini kullanarak oluşturuldu.  
  
 `dwParams`  
 [in] Parametre sayısı `ppParams` dizisi.  
  
 `dwEvalFlags`  
 [in] Bayraklarının bir birleşimi [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md) nasıl gerçekleştirilecek bir değerlendirme olduğunu belirten sabit listesi.  
  
 `dwTimeout`  
 [in] Bu yöntemden geri dönmeden önce beklenecek milisaniye cinsinden en uzun süreyi belirtir. Kullanım **SONSUZ** süresiz bekleme.  
  
 `ppResult`  
 [out] Döndürür bir **IDebugObject** temsil eden bir nesne olarak işlevin değeri.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugFunctionObject2](../../../extensibility/debugger/reference/idebugfunctionobject2.md)

