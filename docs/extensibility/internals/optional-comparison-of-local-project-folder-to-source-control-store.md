---
title: Proje klasörünün kaynak denetimi Store karşılaştırın | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, comparing versions
- source control plug-ins, local project folders
ms.assetid: 65217e8b-15a6-4446-92b0-4cff1c6220f5
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d675868e10a99a192681c52495ad3b37e384d390
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350700"
---
# <a name="optional-comparison-of-local-project-folder-to-source-control-store"></a>İsteğe Bağlı Olarak Yerel Proje Klasörünün Kaynak Denetimi Deposuyla Karşılaştırılması
Kaynak Denetim eklentisi API işlevleri kullanarak yerel proje klasörünün kaynak denetimi arasındaki karşılaştırma gerçekleştirilir 1.2 [Sccdirqueryınfo](../../extensibility/sccdirqueryinfo-function.md) ve [SccDirDiff](../../extensibility/sccdirdiff-function.md).

 İçinde **Çözüm Gezgini**, tek bir dosyayı yerine bir klasör seçtiyseniz **sürümleri Karşılaştır** kısayol menüsünde Yeni çağırır [Sccdirqueryınfo](../../extensibility/sccdirqueryinfo-function.md) ve [ SccDirDiff](../../extensibility/sccdirdiff-function.md) kaynak denetimi eklentisi içinde.

## <a name="new-capability-flags"></a>Yeni özellik bayrakları
 `SCC_CAP_DIRECTORYDIFF`

 `SCC_CAP_DIRECTORYCHECKOUT`

## <a name="new-functions"></a>Yeni işlevleri
- [SccDirDiff](../../extensibility/sccdirdiff-function.md)

- [SccDirQueryInfo](../../extensibility/sccdirqueryinfo-function.md)

 `SccDirQueryInfo` İşlevi önce çağrılır `SccDirDiff` çalışma dizini kaynak-denetimli olup olmadığını belirlemek için. `SccDirDiff` İşlevi, geçerli yerel dizin ve karşılık gelen kaynak denetim klasörü arasındaki farkları görüntüler. Bu komut, kaynak denetimi eklentisi dizine değişikliklerin listesini görüntülemek için sorar. Kaynak Denetimi Eklentisi farkları görüntülemek için kendi kullanıcı Arabirimi sağlar.

> [!NOTE]
> Bu işlev, aynı komut bayrakları olarak kullanır [SccDiff](../../extensibility/sccdiff-function.md). Kaynak Denetimi Eklentisi sağlayıcısı, "hızlı fark" işlemi için dizinleri desteklemeyen tercih edebilirsiniz.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentisi API Sürümü 1.2’deki Yenilikler](../../extensibility/internals/what-s-new-in-the-source-control-plug-in-api-version-1-2.md)