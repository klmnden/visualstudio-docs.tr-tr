---
title: İsteğe bağlı yerel proje klasörünün kaynak denetimi Store karşılaştırması | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, comparing versions
- source control plug-ins, local project folders
ms.assetid: 65217e8b-15a6-4446-92b0-4cff1c6220f5
caps.latest.revision: 15
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 34b9a7ff7d4cc70863090957060db90edfd016b5
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54765745"
---
# <a name="optional-comparison-of-local-project-folder-to-source-control-store"></a>İsteğe Bağlı Olarak Yerel Proje Klasörünün Kaynak Denetimi Deposuyla Karşılaştırılması
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Kaynak Denetim eklentisi API işlevleri kullanarak yerel proje klasörünün kaynak denetimi arasındaki karşılaştırma gerçekleştirilir 1.2 [Sccdirqueryınfo](../../extensibility/sccdirqueryinfo-function.md) ve [SccDirDiff](../../extensibility/sccdirdiff-function.md).  
  
 İçinde **Çözüm Gezgini**, tek bir dosyayı yerine bir klasör seçtiyseniz **sürümleri Karşılaştır** kısayol menüsünde Yeni çağırır [Sccdirqueryınfo](../../extensibility/sccdirqueryinfo-function.md) ve [ SccDirDiff](../../extensibility/sccdirdiff-function.md) kaynak denetimi eklentisi içinde.  
  
## <a name="new-capability-flags"></a>Yeni özellik bayrakları  
 `SCC_CAP_DIRECTORYDIFF`  
  
 `SCC_CAP_DIRECTORYCHECKOUT`  
  
## <a name="new-functions"></a>Yeni işlevleri  
 [SccDirDiff](../../extensibility/sccdirdiff-function.md)  
  
 [SccDirQueryInfo](../../extensibility/sccdirqueryinfo-function.md)  
  
 `SccDirQueryInfo` İşlevi önce çağrılır `SccDirDiff` çalışma dizini kaynak-denetimli olup olmadığını belirlemek için. `SccDirDiff` İşlevi, geçerli yerel dizin ve karşılık gelen kaynak denetim klasörü arasındaki farkları görüntüler. Bu komut, kaynak denetimi eklentisi dizine değişikliklerin listesini görüntülemek için sorar. Kaynak Denetimi Eklentisi farkları görüntülemek için kendi kullanıcı Arabirimi sağlar.  
  
> [!NOTE]
>  Bu işlev, aynı komut bayrakları olarak kullanır [SccDiff](../../extensibility/sccdiff-function.md). Kaynak Denetimi Eklentisi sağlayıcısı, "hızlı fark" işlemi için dizinleri desteklemeyen tercih edebilirsiniz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kaynak Denetimi Eklentisi API Sürümü 1.2’deki Yenilikler](../../extensibility/internals/what-s-new-in-the-source-control-plug-in-api-version-1-2.md)
