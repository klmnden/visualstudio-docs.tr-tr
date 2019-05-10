---
title: Hedef derleme sırası | Microsoft Docs
ms.date: 05/02/2019
ms.topic: conceptual
helpviewer_keywords:
- msbuild, build order
ms.assetid: f4a26339-9f9a-497a-9aa6-0797183d450d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 502cc7d5f1124ef815455193f00c3f30e77c59a8
ms.sourcegitcommit: 6196d0b7fdcb08ba6d28a8151ad36b8d1139f2cc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65225959"
---
# <a name="target-build-order"></a>Hedef derleme sırası

Başka bir hedef üzerinde çıkışını bir hedef girişi bağlıysa hedefleri sıralanmış olmaları gerekmektedir. Bu öznitelikler, hedef çalıştığı sırayı belirtmek için kullanabilirsiniz:

- `InitialTargets`. Bu `Project` özniteliği belirtir önce çalıştırılacak hedeflerin hedefleri komut satırında veya belirtilmese bile `DefaultTargets` özniteliği.

- `DefaultTargets`. Bu `Project` özniteliği belirtir hedefleri çalıştırın hedef komut satırında açıkça belirtilmediği takdirde.

- `DependsOnTargets`. Bu `Target` özniteliği, bu hedef çalıştırmadan önce çalıştırılması gereken hedefleri belirtir.

- `BeforeTargets` ve `AfterTargets`. Bunlar `Target` öznitelikler bu hedeften önce veya sonra belirtilen hedefleri (MSBuild 4.0) çalışması gerektiğini belirtin.

  Bir sonraki hedef yapı ona bağlı olsa bile bir hedef hiçbir zaman bir yapı sırasında iki kez çalıştırın. Bir hedef çalıştırıldıktan sonra kendi derleme katkısı tamamlanmıştır.

  Hedefleri olabilir bir `Condition` özniteliği. Belirtilen koşulun değerlendirme sonucu `false`, hedef yürütülen değildir ve yapı üzerinde hiçbir etkisi olmaz. Koşullar hakkında daha fazla bilgi için bkz. [koşullar](../msbuild/msbuild-conditions.md).

## <a name="initial-targets"></a>Başlangıç hedefleri

 `InitialTargets` Özniteliği [proje](../msbuild/project-element-msbuild.md) öğesi belirtir önce çalıştırılacak hedeflerin hedefleri komut satırında veya belirtilmese bile `DefaultTargets` özniteliği. Başlangıç hedefleri genellikle hata denetlemek için kullanılır.

 Değerini `InitialTargets` özniteliği hedeflerin noktalı virgülle ayrılmış, sıralı bir listesi olabilir. Aşağıdaki örnek belirten `Warm` hedef çalışır ve ardından `Eject` hedef çalıştırır.

```xml
<Project InitialTargets="Warm;Eject" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
```

 İçeri aktarılan projeleri olabilir, kendi `InitialTargets` öznitelikleri. Tüm ilk hedefleri araya toplanır ve sırayla çalıştırın.

 Daha fazla bilgi için [nasıl yapılır: İlk olarak oluşturmak için hangi hedef belirtin](../msbuild/how-to-specify-which-target-to-build-first.md).

## <a name="default-targets"></a>Varsayılan hedefler

 `DefaultTargets` Özniteliği [proje](../msbuild/project-element-msbuild.md) öğesi belirtir hangi hedef veya hedefleri yerleşik bir hedef komut satırında açıkça belirtilmezse.

 Değerini `DefaultTargets` özniteliği varsayılan hedeflerin noktalı virgülle ayrılmış, sıralı bir listesi olabilir. Aşağıdaki örnek belirten `Clean` hedef çalışır ve ardından `Build` hedef çalıştırır.

```xml
<Project DefaultTargets="Clean;Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
```

 Varsayılan hedefler kullanarak kılabilirsiniz **-hedef** anahtarını komut satısına. Aşağıdaki örnek belirten `Build` hedef çalışır ve ardından `Report` hedef çalıştırır. Bu şekilde hedefleri belirttiğinizde, tüm varsayılan hedefleri göz ardı edilir.

 `msbuild -target:Build;Report`

 Hem başlangıç hedefleri hem de varsayılan hedefler belirtilirse ve komut satırı hiçbir hedef belirtilmemişse, MSBuild hedefleri ilk önce çalışır ve ardından varsayılan hedefler çalıştırır.

 İçeri aktarılan projeleri olabilir, kendi `DefaultTargets` öznitelikleri. İlk `DefaultTargets` karşılaştı öznitelik hedefleri çalıştırılacağı hangi varsayılan belirler.

 Daha fazla bilgi için [nasıl yapılır: İlk olarak oluşturmak için hangi hedef belirtin](../msbuild/how-to-specify-which-target-to-build-first.md).

## <a name="first-target"></a>İlk hedef

 Varsa hiçbir ilk hedefler, varsayılan hedefler ya da komut satırı hedefleri ilk hedef MSBuild çalıştırır daha sonra proje dosyası veya içeri aktarılan tüm proje dosyaları karşılaşır.

## <a name="target-dependencies"></a>Hedef bağımlılıklar

 Hedefler birbirleri ile bağımlılık ilişkiler tanımlayabilirsiniz. `DependsOnTargets` Öznitelik, bir hedef diğer hedeflerde bağlı olduğunu gösterir. Örneğin,

```xml
<Target Name="Serve" DependsOnTargets="Chop;Cook" />
```

 MSBuild, söyler `Serve` hedef bağlıdır `Chop` hedef ve `Cook` hedef. MSBuild çalıştıran `Chop` hedef ve çalışan `Cook` çalıştırılmadan önce hedef `Serve` hedef.

## <a name="beforetargets-and-aftertargets"></a>BeforeTargets ve AfterTargets

 MSBuild 4. 0'da, kullanarak hedef sırası belirtebilirsiniz `BeforeTargets` ve `AfterTargets` öznitelikleri.

 Aşağıdaki komut dosyası düşünün.

```xml
<Project DefaultTargets="Compile;Link" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
    <Target Name="Compile">
        <Message Text="Compiling" />
    </Target>
    <Target Name="Link">
        <Message Text="Linking" />
    </Target>
</Project>
```

 Bir ara hedefi oluşturmak için `Optimize` sonra çalışan `Compile` hedef, ancak önce `Link` hedef, aşağıdaki hedef herhangi bir yere ekleyin `Project` öğesi.

```xml
<Target Name="Optimize"
    AfterTargets="Compile" BeforeTargets="Link">
    <Message Text="Optimizing" />
</Target>
```

## <a name="determine-the-target-build-order"></a>Hedef derleme sırasını belirleme

 MSBuild hedef derleme sırası gibi belirler:

1. `InitialTargets` hedefleri çalıştırılır.

2. Komut satırı tarafından belirtilen hedefleri **-hedef** anahtar çalıştırılır. Hiçbir hedef komut satırında belirtin, ardından `DefaultTargets` hedefleri çalıştırın. Ardından ikisi de mevcutsa karşılaşılan ilk hedef çalıştırılır.

3. `Condition` Özniteliği hedef değerlendirilir. Varsa `Condition` özniteliği var ve değerlendiren `false`, hedef yürütülen değildir ve yapı üzerinde başka hiçbir etkisi olmaz.

    Koşullu hedef listesinde diğer hedeflerden `BeforeTargets` veya `AfterTargets` hala önceden belirlenmiş bir sırada yürütün.

4. Hedef yürütülen veya atlandı, önce kendi `DependsOnTargets` hedefleri çalıştırılır, sürece `Condition` özniteliği hedef uygulanır ve değerlendiren `false`.

   > [!NOTE]
   > Bir hedef atlandı, çıkış öğeleri güncel olduğundan yürütülmez ise olarak kabul edilir (bkz [Artımlı derleme](../msbuild/incremental-builds.md)). Bu onay, hedef içindeki görevlerin yürütmeden önce gerçekleştirilir ve hedeflerin yürütme sırası etkilemez.

5. Hedef yürütülen veya hedef listeler herhangi bir hedef atlandı önce bir `BeforeTargets` özniteliği çalıştırılır.

6. Hedef yürütülmeden önce kendi `Inputs` özniteliği ve `Outputs` özniteliği karşılaştırılır. MSBuild belirlerse herhangi bir çıktı dosyalarını karşılık gelen girdi dosyası veya dosya ile ilgili güncel değil ve MSBuild hedefi yürütür. Aksi takdirde, MSBuild hedefini atlar.

7. Hedef yürütülen veya içinde listeler herhangi bir hedef atlandı sonra bir `AfterTargets` özniteliği çalıştırılır.

## <a name="see-also"></a>Ayrıca bkz.

- [Hedefler](../msbuild/msbuild-targets.md)
