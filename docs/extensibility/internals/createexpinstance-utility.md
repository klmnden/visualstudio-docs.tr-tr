---
title: Createexpınstance yardımcı programı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- experimental builds
- experimental hive
- experimental instance
- createexpinstance
- createexpinst
ms.assetid: 03779774-9401-49ae-997c-0c3ab25ed0d5
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ed03833b6c109ca78feb86c1cfe41fa453022c66
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66341910"
---
# <a name="createexpinstance-utility"></a>Createexpınstance yardımcı programı
Kullanım **Createexpınstance** oluşturmak, sıfırlama veya Visual Studio'nun deneysel örneği silmek için yardımcı program. Deneysel örneğinde hata ayıklayın ve Visual Studio uzantıları temel ürünü değiştirmeden test etmek için kullanabilirsiniz.

## <a name="syntax"></a>Sözdizimi

```
CreateExpInstance.exe [/Create | /Reset | /Clean] /VSInstance=VsInstance /RootSuffix=Suffix
```

## <a name="parameters"></a>Parametreler
 **/ Oluşturma** deneysel örneği oluşturur.

 **/ Sıfırlama** Deneysel örneğini siler ve ardından yeni bir tane oluşturur.

 **/ Clean** Deneysel örneğini siler.

 **/ VSInstance** kopyalamak için temel Visual Studio örneğini içeren dizinin adı.

 **/ RootSuffix** deneysel örneği dizin adının sonuna eklenecek sonek.

## <a name="remarks"></a>Açıklamalar
 Visual Studio uzantısı üzerinde çalışırken, varsayılan deneysel örneğinde açın ve geçerli uzantıyı yüklemek için F5 tuşuna basabilirsiniz. Deneysel örnek varsa, varsayılan ayarlara sahip bir Visual Studio oluşturur.

 Deneysel örneği varsayılan konumu, Visual Studio sürüm sayısına bağlıdır. Örneğin, Visual Studio 2015 için konumdur *%localappdata%\Microsoft\VisualStudio\14.0Exp\\* . Tüm dosyaları dizin konumu, örnek bir parçası olarak kabul edilir. Dizin adı varsayılan konuma değiştirilmediği sürece, herhangi bir ek deneysel örneği Visual Studio tarafından yüklenmez.

 Visual Studio deneysel örneği açıldığında, sistem kayıt defteri erişimi yoktur. Bu, kullanılan kayıt defteri kovanını Deneysel bir sürümü Visual Studio'nun önceki sürümlerden farklıdır.

 **Createexpınstance** yardımcı programı değiştirir **VsRegEx** yardımcı programı.

 Aşağıdaki örnek, Visual Studio varsayılan Deneysel örneğini sıfırlar:

 **CreateExpInstance.exe Reset /VSInstance 14.0 = /RootSuffix Exp =**

## <a name="see-also"></a>Ayrıca bkz.
- [VSPackage’lar](../../extensibility/internals/vspackages.md)