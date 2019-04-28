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
ms.openlocfilehash: 965147083bdc11a3544561fdd96cd85221ccd443
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63410144"
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
> Bu yöntem ilgilendiğiniz iş parçacığı içinde çağrılır. Bu, geçerli iş parçacığı tanımlamak ve uygun bir numaralandırıcıyı döndürmek için en fazla uygulayan olur.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IProvideExpressionContexts Arabirimi](../../winscript/reference/iprovideexpressioncontexts-interface.md)