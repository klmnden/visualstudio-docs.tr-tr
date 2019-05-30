---
title: Kaynak denetimi eklentileri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, reference
ms.assetid: 964980ca-21c5-4706-8535-6ea23e1c9cc9
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 01e7a0ca8a509d430a0794a2cedb4b2e9d869585
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66331825"
---
# <a name="source-control-plug-ins"></a>Kaynak Denetimi Eklentileri
Kaynak Denetimi Eklentisi SDK başvuru bölümüne ile tümleşik kaynak denetimi sistemlerini sağlayan eksiksiz arabirim belirtimi içeren [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Sözdizimi ve semantiği ile arabirim oluşturmak için kaynak denetimi eklentisi uygulamalıdır çeşitli işlevleri ve veri türlerini belirtir [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] tümleşik geliştirme ortamı (IDE).

## <a name="in-this-section"></a>Bu Bölümde
- [Kaynak Denetimi Eklentisi API işlevleri](../extensibility/source-control-plug-in-api-functions.md) kaynak denetimi eklentisi API ile uyum sağlamak için kaynak denetimi eklentisi tarafından uygulanması gereken işlevleri listeler.

- [Geri çağırma işlevleri IDE tarafından uygulanan](../extensibility/callback-functions-implemented-by-the-ide.md) belirli komutları yürütülürken IDE bilgi geçirmek için kaynak denetimi eklentisi kullanan işlevler açıklanmaktadır.

- [Numaralandırıcılar](../extensibility/enumerators.md) kaynak denetimi eklentisi hakkında bilmeniz gereken kaynak denetimi eklentisi API Numaralandırıcı veri türlerini listeler.

- [Özellik bayrakları](../extensibility/capability-flags.md) Describes `SCC_CAP_xxx` bir sağlayıcının özelliklerini gösteren bayrak.

- [Kullanılan bit bayrakları tarafından belirli komutları](../extensibility/bitflags-used-by-specific-commands.md) belirli komutları bağlamında yararlıdır bayrakları listeler.

- [Hata kodları](../extensibility/error-codes.md) işlevleri tarafından döndürülen genel hata değerlerini listeler `SCCTRN`.

- [Kaynak denetimi eklentisi bulmak için anahtar olarak kullanılan dizeler](../extensibility/strings-used-as-keys-for-finding-a-source-control-plug-in.md) kaynak denetimi eklentisi bulmak için kayıt defteri erişim tuşları açıklanmaktadır.

- [MSSCCPRJ. SCC dosya](../extensibility/mssccprj-scc-file.md) IDE'ye donuk bilgileri içeren, ancak kaynak denetimi eklentisi tarafından sürüm denetimine çözüm veya projeyi bulmak için kullanılan bir istemci-tarafı dosya açıklar.

- [Kaynak Denetimi Eklentisi uygulamak için en iyi uygulamalar](../extensibility/best-practices-for-implementing-a-source-control-plug-in.md) kaynak denetimi eklentisi API uyguladığınız sırada hatırlamak önemli teknik anımsatıcılar sağlar.

- [Dize uzunluğu kısıtlamaları](../extensibility/restrictions-on-string-lengths.md) çeşitli işlevler için kullanılan dizelerin uzunluklarının kaynak denetimi eklentisi API kısıtlamaları açıklar.

- [Sözlük](../extensibility/source-control-plug-in-glossary.md) yararlı hüküm ve kaynak denetimi eklentisi SDK belgeleri okumak için tanımlarını sağlar.

- [Nasıl yapılır: Kapatma kapatmak için uyumluluk uyarılarını kaynak denetimi eklentileri](../extensibility/how-to-turn-off-compatibility-warnings-for-source-control-plug-ins.md) uyarıları devre dışı bırakma açıklar.

## <a name="related-sections"></a>İlgili Bölümler
- [Kaynak Denetimi Eklentisi örnek](https://www.microsoft.com/download/details.aspx?id=55984) kaynak denetimi eklentisi işlevlerini bir örneğini sağlar.

- [Test kaynak denetimi eklentileri için Kılavuzu](../extensibility/internals/test-guide-for-source-control-plug-ins.md) kaynak denetimi eklentisi ile ilgili sınama yordamları açıklar.

- [Kaynak Denetimi Eklentisi oluşturma](../extensibility/internals/creating-a-source-control-plug-in.md) kaynak denetimi işlevlerini kullanırken sağlayan bir kaynak denetimi eklentisi oluşturma anlatılmaktadır [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] kaynak denetimi kullanıcı arabirimini (UI).

- [Visual Studio SDK başvurusu](../extensibility/visual-studio-sdk-reference.md) başvuru konuları bir listesini sunar.