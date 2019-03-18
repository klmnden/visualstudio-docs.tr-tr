---
title: IProvideExpressionContexts::EnumExpressionContexts | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IProvideExpressionContexts.EnumExpressionContexts
apilocation:
- jscript.dll
helpviewer_keywords:
- IProvideExpressionContexts::EnumExpressionContexts
ms.assetid: ec5f0065-00df-41e6-b480-4c04ba464872
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d1e4c462780f7026329ff7a5d22c86dbb6058dc5
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58157756"
---
# <a name="iprovideexpressioncontextsenumexpressioncontexts"></a>IProvideExpressionContexts::EnumExpressionContexts
Bu bileşen tarafından bilinen ifade bağlamları bir numaralandırıcı döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT EnumExpressionContexts(  
   IEnumDebugExpressionContexts**  ppedec  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppedec`  
 [out] Bu bileşen tarafından bilinen ifade bağlamları bir numaralandırıcı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 İşlem Hata Ayıklama Yöneticisi, belirli bir iş parçacığıyla ilişkilendirilmiş tüm genel ifade içerikleri bulmak için bu yöntemi kullanır.  
  
> [!NOTE]
>  Bu yöntem ilgilendiğiniz iş parçacığı içinde çağrılır. Bu, geçerli iş parçacığı tanımlamak ve uygun bir numaralandırıcıyı döndürmek için en fazla uygulayan olur.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IProvideExpressionContexts Arabirimi](../../winscript/reference/iprovideexpressioncontexts-interface.md)