---
title: 'Örnek Excel uzantısı: ActionFilter sınıfı | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-test
ms.topic: conceptual
ms.assetid: c69fe3c7-f797-4e90-b21c-f2cc4dddf152
caps.latest.revision: 13
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 26eb001de3a8fed7c6bb1d9d1a547aa618e745e8
ms.sourcegitcommit: 2da366ba9ad124366f6502927ecc720985fc2f9e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68871609"
---
# <a name="sample-excel-extension-actionfilter-class"></a>Örnek Excel uzantısı: ActionFilter Sınıfı
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu iç sınıf [uitestactionfilter](/previous-versions/visualstudio/visual-studio-2012/dd985757(v=vs.110)) sınıfını genişletir ve bir [!INCLUDE[ofprexcel](../includes/ofprexcel-md.md)] öğe üzerindeki test eylemleri için bir filtre temsil eder.

## <a name="simple-properties"></a>Basit özellikler
 Bu salt okunurdur özellikler, geliştiricinin bu test eylemi filtresinin kodlanmış UI test çerçevesi tarafından nasıl çalıştırılacağını belirtmesini sağlar. Örneğin, `UITestActionFilter.Name` özelliği eylem filtresinin adını sağlar. Diğer özellikler, bu `UITestActionFilter.Category` test eylemi filtresi tarafından filtrelenen test `UITestActionFilter.FilterType`eylemlerinin `UITestActionFilter.Group` adını, eylem filtresinin, bu adı alır. Diğer kişiler de test `UITestActionFilter.ApplyTimeout` `UITestActionFilter.Enabled`eyleminin olup olmadığını gösterir.

## <a name="processrule-method"></a>ProcessRule yöntemi
 Bu yöntem, kodlanmış UI test çerçevesi tarafından çağrılır ve filtreyi belirtilen `IUITestActionStack`şekilde yürütür. Bu özel geçersiz kılma, yığındaki bir sonraki eylem, hücreye tuş vuruşları gönderdiğinde bir hücrede fare seçme eylemini kaldırır. Ardından döndürür `false`.

## <a name="private-methods"></a>Özel Yöntemler
 Yöntemi `IsLeftClick` , belirtilen eylemin farenin sol tıklamasını temsil ettiğini belirler. Yöntemi `AreActionsOnSameExcelCell` , Excel 'deki aynı hücrede iki adet belirtilen eylemin yürütülüp yürütülmeyeceğini belirler.

## <a name="see-also"></a>Ayrıca bkz.

- [Kodlanmış Kullanıcı Arabirimi Testlerini ve Eylem Kayıtlarını Microsoft Excel'i Desteklemek için Genişletme](../test/extending-coded-ui-tests-and-action-recordings-to-support-microsoft-excel.md)
