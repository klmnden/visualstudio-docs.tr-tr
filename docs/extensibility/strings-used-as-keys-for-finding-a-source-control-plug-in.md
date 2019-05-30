---
title: Kaynak denetimi eklentisi bulmak için anahtar olarak kullanılan dizeler | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, strings used for finding
ms.assetid: c1e31f76-42a1-4c3d-afb2-664044ef12fd
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 31c2b30fb41976cdbbab13fa22d438c63bddbbef
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66331714"
---
# <a name="strings-used-as-keys-for-finding-a-source-control-plug-in"></a>Kaynak Denetimi Eklentisi Bulmak için Anahtar Olarak Kullanılan Dizeler
Eklenti kaynak denetimi hakkında bilgi bulmak için kayıt defteri erişim tuşları dizelerdir.

 `STR_SCC_PROVIDER_REG_LOCATION`, `STR_PROVIDERREGKEY`, `STR_SCCPROVIDERPATH`, ve `STR_SCCPROVIDERNAME` kayıt defteri anahtarlarını ya da bir DLL için Visual Studio kaynak denetimi eklentisi kaydetmek için kullanılan değerler.

 `SCC_PROJECTNAME_KEY`, `SCC_PROJECTAUX_KEY`, `SCC_KEY, SCC_FILE_SIGNATURE`, ve `SCC_STATUS_FILE` MSSCCPRJ biçimini tanımlamak için kullanılır. SCC dosyası.

## <a name="string-keys-and-values"></a>Dize anahtarları ve değerleri

|Anahtar|Değer|
|---------|-----------|
|`STR_SCC_PROVIDER_REG_LOCATION`|Software\SourceCodeControlProvider|
|`STR_PROVIDERREGKEY`|ProviderRegKey|
|`STR_SCCPROVIDERPATH`|SCCServerPath|
|`STR_SCCPROVIDERNAME`|SCCServerName|
|`STR_SCC_INI_SECTION`|Kaynak kodu denetimi|
|`STR_SCC_INI_KEY`|SourceCodeControlProvider|
|`SCC_PROJECTNAME_KEY`|SCC_Project_Name|
|`SCC_PROJECTAUX_KEY`|SCC_Aux_Path|
|`SCC_STATUS_FILE`|MSSCCPRJ.SCC|
|`SCC_KEY`|SCC|
|`SCC_FILE_SIGNATURE`|Bir kaynak kodu denetim dosyası|
|`SCC_NSE`|Namespace uzantısı|
|`SCC_NSE_PREFIX`|İletişim kuralı ön eki|
|`SCC_NSE_DisableOpenSCC`|DisableOpenFromSourceControl|
|`STR_SCCHELPCOLLECTION`|HelpCollection|
|`STR_UI_LANGUAGE`|UILanguage|
|`STR_SRCSAFE_ROOT_KEY`|Software\Microsoft\SourceSafe|

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentileri](../extensibility/source-control-plug-ins.md)
- [Nasıl yapılır: Kaynak Denetimi Eklentisi Yükleme](../extensibility/internals/how-to-install-a-source-control-plug-in.md)
- [MSSCCPRJ.SCC Dosyası](../extensibility/mssccprj-scc-file.md)