---
title: SetEnv görevi | Microsoft Docs
ms.date: 11/05/2018
ms.topic: reference
f1_keywords:
- vc.task.setenv
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), tasks
- SetEnv task (MSBuild (Visual C++))
ms.assetid: fd9e4225-68cb-4608-8b27-468b0218c936
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 16a73ac066ff0b61570f0ed918308cf8874121d7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62996523"
---
# <a name="setenv-task"></a>SetEnv görevi
Belirtilen ortam değişkeninin değerini siler veya ayarlar.

## <a name="parameters"></a>Parametreler
 Parametreleri aşağıdaki tabloda açıklanmıştır **SetEnv** görev.

|Parametre|Açıklama|
|---------------|-----------------|
|**Ad**|Gerekli **dize** parametresi.<br /><br /> Bir ortam değişkeninin adı.|
|**OutputEnvironmentVariable**|İsteğe bağlı **dize** çıkış parametresi.<br /><br /> Tarafından belirtilen ortam değişkenine atanan değeri içeren **adı** parametresi.|
|**Ön eki**|Zorunlu `Boolean` parametresi.<br /><br /> Varsa `true`, değerini art arda ekler **değer** parametresi tarafından belirtilen ortam değişkeninin değerini önce **adı** parametresi ve ardından sonucu ortama atar değişken. Varsa `false`, yalnızca değerini atar **değer** ortam değişkenine parametresi.|
|**Hedef**|İsteğe bağlı **dize** parametresi.<br /><br /> Bir ortam değişkeni depolandığı konumu belirtir. "Kullanıcı" veya "Machine" belirtin.<br /><br /> Daha fazla bilgi için [EnvironmentVariableTarget numaralandırma](xref:System.EnvironmentVariableTarget).|
|**Değer**|İsteğe bağlı **dize** parametresi.<br /><br /> Tarafından belirtilen ortam değişkenine atanan değeri **adı** parametresi. Varsa **değer** boştur ve değişken var, değişken silindi. Değişkeni mevcut değilse işlemin gerçekleştirilmesinden olsa bile hata oluşmaz.<br /><br /> Daha fazla bilgi için [Environment::SetEnvironmentVariable yöntemi](xref:System.Environment.SetEnvironmentVariable%2A).|

## <a name="see-also"></a>Ayrıca bkz.
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)