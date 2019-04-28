---
title: IDebugApplication110::CallableWaitForHandles | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IDebugApplication110::CallableWaitForHandles
ms.assetid: 02e79b60-0d67-47f9-bf78-b65a02c9c014
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f74e3faa57e9ee4a38f77110334383bc2c72fe2f
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63446388"
---
# <a name="idebugapplication110callablewaitforhandles"></a>IDebugApplication110::CallableWaitForHandles
İzin verirken sinyal belirtilen tutamaçlardan birini bekler bu iş parçacığına yayımlanacak çağrıları iş parçacıkları arası. Bu yöntem, hata ayıklayıcı iş parçacığında çağrılmalıdır.  
  
> [!IMPORTANT]
> [Idebugapplication110 arabirimi](../../winscript/reference/idebugapplication110-interface.md) PDM v11.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT CallableWaitForHandles([in] DWORD handleCount, [in, size_is(handleCount)] const HANDLE* pHandles, [out] DWORD* pIndex);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `handleCount`  
 Bekleme tanıtıcıları sayısı.  
  
 `pHandles`  
 Bekleme tanıtıcıları kümesi.  
  
 `pIndex`  
 HRESULT değerini S_OK, dizine olduğunda `pHandles` sinyal işleyici için.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugApplication110 Arabirimi](../../winscript/reference/idebugapplication110-interface.md)