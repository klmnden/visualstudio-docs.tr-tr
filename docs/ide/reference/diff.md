---
title: -Diff
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
ms.assetid: 5377fedb-632a-4e86-a947-7c11c86451e7
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: cf58c25611fd52c6e8db8e8210101e1c80153275
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53844544"
---
# <a name="diff"></a>/Diff
İki dosyayı karşılaştırır. Farklar, özel bir Visual Studio penceresinde görüntülenir.

## <a name="syntax"></a>Sözdizimi

```cmd
devenv /Diff SourceFile, TargetFile, [SourceDisplayName],[TargetDisplayName]
```

## <a name="arguments"></a>Arguments
 `SourceFile`

 Gerekli. Karşılaştırılacak ilk dosya adını ve tam yolu.

 `TargetFile`

 Gerekli. Karşılaştırılacak ikinci dosyasının adını ve tam yolunu

 `SourceDisplayName`

 İsteğe bağlı. İlk dosya görünen adı.

 `TargetDisplayName`

 İsteğe bağlı. İkinci dosyanın görünen adı.