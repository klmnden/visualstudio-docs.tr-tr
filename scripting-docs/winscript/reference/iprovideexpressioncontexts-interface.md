---
title: Iprovideexpressioncontexts arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IProvideExpressionContexts interface
ms.assetid: e4c70f2c-7d86-4fdc-a1cb-f5a0bb8ed037
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b6ec0d5e17b0d3527252352c2e789adfac4fa859
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63410058"
---
# <a name="iprovideexpressioncontexts-interface"></a>IProvideExpressionContexts Arabirimi
Belirli bir bileşen tarafından bilinen ifade bağlamları listelemek için bir yol sağlar. Komut dosyası motorları, genellikle bu arabirimi uygulayın.  
  
 İşlem Hata Ayıklama Yöneticisi bu arabirimi belirli bir iş parçacığıyla ilişkilendirilmiş tüm genel ifade içerikleri bulmak için kullanır.  
  
> [!NOTE]
> Bu arabirim ilgilendiğiniz iş parçacığı içinde çağrılır. Bu, geçerli iş parçacığı tanımlamak ve uygun bir numaralandırıcıyı döndürmek için en fazla uygulayan olur.  
  
## <a name="methods"></a>Yöntemler  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IProvideExpressionContexts` arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IProvideExpressionContexts::EnumExpressionContexts](../../winscript/reference/iprovideexpressioncontexts-enumexpressioncontexts.md)|Bu bileşen tarafından bilinen ifade bağlamları bir numaralandırıcı döndürür.|