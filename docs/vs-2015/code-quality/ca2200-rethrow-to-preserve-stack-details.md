---
title: 'CA2200: Yığın ayrıntılarını korumak için yeniden fırlatma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- RethrowToPreserveStackDetails
- CA2200
helpviewer_keywords:
- CA2200
- RethrowToPreserveStackDetails
ms.assetid: 046e1b98-c4dc-4515-874f-9c0de2285621
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: ed2dd2884268511ae05ac89c132f73fdf8b2771e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68201639"
---
# <a name="ca2200-rethrow-to-preserve-stack-details"></a>CA2200: Yığın ayrıntılarını korumak için yeniden fırlatın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|RethrowToPreserveStackDetails|
|CheckId|CA2200|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Bir özel durum yeniden ve özel durum açıkça belirtilen `throw` deyimi.

## <a name="rule-description"></a>Kural Tanımı
 Bir özel durum sonra bunu izleme bilgileri parçası yığın izlemesi aşağıdadır. Yığın izlemesi, özel durum oluşturur ve özel durumu yakalar yöntemi ile biten yöntem ile başlayan yöntemi çağrı hiyerarşisini listesidir. Özel durum belirterek yeniden durum varsa `throw` deyimi, yığın izlemesi geçerli bir yöntem yeniden başlatılır ve özel durum döndüren özgün yöntem ile geçerli yöntemi arasındaki yöntem çağrılarını listesini kaybolur. Özel durum ile özgün yığın izleme bilgileri tutmak için kullanın `throw` özel durum belirtmeden deyimi.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için özel durum açıkça belirtmeden bir özel durum yeniden oluşturun.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bir yöntemi gösterir `CatchAndRethrowExplicitly`, kural ve bir yöntem ihlal `CatchAndRethrowImplicitly`, kural karşılar.

 [!code-csharp[FxCop.Usage.Rethrow#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.Rethrow/cs/FxCop.Usage.Rethrow.cs#1)]
 [!code-vb[FxCop.Usage.Rethrow#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.Rethrow/vb/FxCop.Usage.Rethrow.vb#1)]
