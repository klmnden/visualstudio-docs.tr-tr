---
title: Visual Studio'da hiyerarşiler | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- hierarchies, Visual Studio IDE
- IDE, hierarchies
ms.assetid: 0a029a7c-79fd-4b54-bd63-bd0f21aa8d30
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 29eb35e807c467b64a89f48705c555d4083ceef7
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66328854"
---
# <a name="hierarchies-in-visual-studio"></a>Visual Studio’da Hiyerarşiler
[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Tümleşik geliştirme ortamı (IDE) proje olarak görüntüleyen bir *hiyerarşi*. IDE içinde bir hiyerarşi, her düğüme bir ilişkili özellikler kümesini sahip olduğu düğümlerinin ağacıdır. A *proje hiyerarşisi* proje öğelerini, öğeleri ilişkileri ve öğeleri ilişkili özellikler ve komutları tutan bir kapsayıcıdır.

 İçinde [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], hiyerarşi arabirimini kullanarak proje hiyerarşileri Yönet <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy>. <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy> Arabirimi, proje öğeleri için çağırma standart komut işleyici yerine uygun hiyerarşisi penceresi komutları yönlendirir.

## <a name="project-hierarchies"></a>Proje hiyerarşiler
 Her proje hiyerarşisi, görüntüleyebileceği ve düzenleyebileceği öğeleri içerir. Bu öğeler, proje türüne göre değişiklik gösterir. Örneğin, bir veritabanı projesi veritabanı tabloları, veritabanı görünümlerini ve saklı yordamlarını içerebilir. Bir programlama dili proje Öte yandan, büyük olasılıkla kaynak dosyaları ve bit eşlemler ve iletişim kutuları için kaynak dosyaları içerir. Bir proje hiyerarşisi oluşturduğunuzda, bazı ek esneklik sağlayan hiyerarşileri yuvalanabilir.

 Yeni bir proje türü oluşturduğunuzda, proje türü içinde düzenlenebilir öğeleri tam kümesini denetler. Ancak, projeleri düzenleme desteği sahip oldukları olmayan öğeler içerebilir. Örneğin, Visual C++, HTML dosya türü için özelleştirilmiş bir düzenleyici sağlamaz olsa da Visual C++ projeleri HTML dosyaları içerebilir.

 Kalıcılık içerdikleri öğelerin hiyerarşileri Yönet. Uygulama hiyerarşisi hiyerarşi içinde öğelerin Kalıcılık etkileyen herhangi bir özel özellikler denetim gerekir. Örneğin, öğeleri deposundaki dosyaları yerine nesneleri temsil ediyorsa, hiyerarşi uygulama söz konusu nesnelerin Kalıcılık kontrol gerekir. IDE uyumlu kullanıcı girişi öğelerini kaydetmek için hiyerarşi yönlendirir, ancak IDE öğeleri kaydetmek için gereken tüm eylemleri denetlemez. Bunun yerine, denetiminde projesidir.

 Bir kullanıcı bir öğe bir düzenleyicide açıldığında, o öğe denetimleri hiyerarşi seçilir ve etkin olan hiyerarşi haline gelir. Seçili hiyerarşiyi bir öğeye hareket kullanılabilir komutları kümesini belirler. Bu şekilde kullanıcı odağı izleme, kullanıcının geçerli bağlam yansıtacak şekilde hiyerarşi sağlar.

## <a name="see-also"></a>Ayrıca bkz.
- [Proje türleri](../../extensibility/internals/project-types.md)
- [Seçim ve para birimi IDE](../../extensibility/internals/selection-and-currency-in-the-ide.md)
- [VSSDK örnekleri](https://aka.ms/vs2015sdksamples)