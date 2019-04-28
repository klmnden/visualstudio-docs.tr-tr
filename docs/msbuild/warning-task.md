---
title: Uyarı görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Warning
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- Warning task [MSBuild]
- MSBuild, Warning task
ms.assetid: 96ba5507-8b43-4f54-a1d7-9b15644dd56c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: afbf7dd2f8ae42cd21ee7c9d006d9f503d2d3bf9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62779097"
---
# <a name="warning-task"></a>Uyarı görevi
Günlükleri bir derleme sırasında bir uyarı değerlendirilen bir koşullu ifadeye göre.

## <a name="parameters"></a>Parametreler
 Parametreleri aşağıdaki tabloda açıklanmıştır `Warning` görev.

| Parametre | Açıklama |
|---------------| - |
| `Code` | İsteğe bağlı `String` parametresi.<br /><br /> Uyarıyla ilişkilendirilecek uyarı kodu. |
| `File` | İsteğe bağlı `String` parametresi.<br /><br /> Varsa ilgili dosyayı belirtir. Uyarı görevi içeren dosyayı herhangi bir dosya sağlanırsa, kullanılır. |
| `HelpKeyword` | İsteğe bağlı `String` parametresi.<br /><br /> Uyarıyla ilişkilendirilecek Yardım anahtar sözcüğü. |
| `Text` | İsteğe bağlı `String` parametresi.<br /><br /> Uyarı metni, [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] günlüğe `Condition` parametresi değerlendirilen `true`. |

## <a name="remarks"></a>Açıklamalar
 `Warning` Görev sağlayan [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] gerekli yapılandırma veya bir sonraki devam etmeden önce özellik varlığını denetlemek için projeleri derleme adımı.

 Varsa `Condition` parametresinin `Warning` görev değerlendirilen `true`, değerini `Text` parametresi günlüğe kaydedilir ve yürütmek yapı devam eder. Varsa bir `Condition` parametresi mevcut değil, uyarı metni günlüğe kaydedilir. Günlüğe kaydetme hakkında daha fazla bilgi için bkz. [elde derleme günlükleri](../msbuild/obtaining-build-logs-with-msbuild.md).

 Yukarıda listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.TaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.Task> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [TaskExtension taban sınıfı](../msbuild/taskextension-base-class.md).

## <a name="example"></a>Örnek
 Aşağıdaki kod örneği, komut satırında ayarlanan özellikler denetler. Özellikleri ayarlanmadı varsa, projeye bir uyarı olayını başlatır ve değerini günlüklerini `Text` parametresinin `Warning` görev.

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
    <Target Name="ValidateCommandLine">
        <Warning
            Text=" The 0 property was not set on the command line."
            Condition="'$(0)' == ''" />
        <Warning
            Text=" The FREEBUILD property was not set on the command line."
            Condition="'$(FREEBUILD)' == ''" />
    </Target>
    ...
</Project>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Derleme günlükleri alın](../msbuild/obtaining-build-logs-with-msbuild.md)
- [Proje dosyası şema başvurusu](../msbuild/msbuild-project-file-schema-reference.md)