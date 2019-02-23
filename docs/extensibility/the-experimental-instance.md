---
title: Deneysel örneği | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- experimental builds
- VSPackages, experimental builds
- VSIP, experimental builds
ms.assetid: ead0df4e-6f88-4b42-9297-581b7902f050
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8c4aa7e8e74ccb8f31dc2320192cf088b5391678
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56685124"
---
# <a name="the-experimental-instance"></a>Deneysel Örnek
Visual Studio geliştirme ortamınızı değişiklik yapmış olabilir, test edilmemiş uygulamalardan korumak için VSSDK denemek için kullanabileceğiniz bir Deneysel alanı sağlar. Visual Studio zamanki kullanarak yeni uygulamalar geliştirin, ancak bunları bu deneysel örneği kullanarak çalıştırın.

 Bir VSIX paketi olan her bir uygulama, hata ayıklama modunda Visual Studio deneysel örneği başlatır.

 Visual Studio'nun deneysel örneğinde belirli bir çözüm dışında başlatmak istiyorsanız, komut penceresinde aşağıdaki komutu çalıştırın:

 "*\<Visual studio yükleme yolu >* \Common7\IDE\devenv.exe" RootSuffix üs

> [!NOTE]
>  Deneysel örneği altındaki kayıt defterine yazılır `<version number>Exp` ve `<version number>Exp_Config` düğümleri. Örneğin Visual Studio 2015 Deneysel kayıt defteri alandır
>
>  `HKCU\Software\Microsoft\VisualStudio\14.0Exp` ve `HKCU\Software\Microsoft\VisualStudio\14.0Exp_Config`

 Bunu geliştirirken deneysel örneğinde uzantınızı çalıştırmanızı öneririz. Uzantı dağıttığınızda, geliştirme örneğinde çalışır. Uygulamaları kaydetme hakkında daha fazla bilgi için bkz. [VSPackage kaydetme](../extensibility/internals/registering-vspackages.md).