---
title: Iprovideexpressioncontexts arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 91f4251fec57001ba6c7a4ea1804ec72371418bb
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54345103"
---
# <a name="iprovideexpressioncontexts-interface"></a>IProvideExpressionContexts Arabirimi
Belirli bir bileşen tarafından bilinen ifade bağlamları listelemek için bir yol sağlar. Komut dosyası motorları, genellikle bu arabirimi uygulayın.  
  
 İşlem Hata Ayıklama Yöneticisi bu arabirimi belirli bir iş parçacığıyla ilişkilendirilmiş tüm genel ifade içerikleri bulmak için kullanır.  
  
> [!NOTE]
>  Bu arabirim ilgilendiğiniz iş parçacığı içinde çağrılır. Bu, geçerli iş parçacığı tanımlamak ve uygun bir numaralandırıcıyı döndürmek için en fazla uygulayan olur.  
  
## <a name="methods"></a>Yöntemler  
 Devralınan yöntemleri yanı sıra `IUnknown`, `IProvideExpressionContexts` arabirimi aşağıdaki yöntemleri sunar.  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[IProvideExpressionContexts::EnumExpressionContexts](../../winscript/reference/iprovideexpressioncontexts-enumexpressioncontexts.md)|Bu bileşen tarafından bilinen ifade bağlamları bir numaralandırıcı döndürür.|