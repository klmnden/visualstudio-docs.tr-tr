---
title: CPPClean görevi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
f1_keywords:
- vc.task.cppclean
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), CPPClean task
- CPPClean task (MSBuild (Visual C++))
ms.assetid: b62a482e-8fb5-4999-b50b-6605a078e291
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: bddba1170cf675b5bde7ab8deed8cce1e7eb57dd
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68196569"
---
# <a name="cppclean-task"></a>CPPClean Görevi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

MSBuild Visual C++ proje derlenirken oluşturan geçici dosyaları siler. Derleme dosyaları silme işlemi olarak bilinir *Temizleme*.  

## <a name="parameters"></a>Parametreler  
 Parametreleri aşağıdaki tabloda açıklanmıştır **CPPClean** görev.  

|            Parametre            |                                                                                                Açıklama                                                                                                 |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        **DeletedFiles**         |                               İsteğe bağlı `ITaskItem[]` çıkış parametresi.<br /><br /> Tüketilen ve görevler tarafından yayılan MSBuild çıkış dosya öğeleri bir dizisi tanımlanmaktadır.                                |
|          **DoDelete**           |                                                            İsteğe bağlı **Boole** parametresi.<br /><br /> Varsa `true`, temiz geçici dosyaları derleme.                                                             |
| **FilePatternsToDeleteOnClean** |                                            Gerekli `String` parametresi.<br /><br /> Noktalı virgülle ayrılmış bir temizlemeye dosyaların dosya uzantıları listesini belirtir.                                             |
|   **FilesExcludedFromClean**    |                                                    İsteğe bağlı `String` parametresi.<br /><br /> Dosyaları değil temizlemek için noktalı virgül ile ayrılmış bir listesini belirtir.                                                    |
|       **FoldersToClean**        | Gerekli `String` parametresi.<br /><br /> Temizlemek için dizinlerin noktalı virgülle ayrılmış bir listesini belirtir. Tam veya göreli bir yol belirtin ve yolun joker karakter sembolünü içermelidir ( **\\** \*). |

## <a name="remarks"></a>Açıklamalar  

## <a name="see-also"></a>Ayrıca Bkz.  
 [Görev Başvurusu](../msbuild/msbuild-task-reference.md)
