---
title: Python kodunu PyLint kullanma
description: PyLint linting özelleştirmek için komut satırı seçenekleri dahil olmak üzere Python kodunda sorunlarını denetlemek için Visual Studio'da çalıştırın.
ms.date: 03/13/2019
ms.topic: conceptual
author: JoshuaPartlow
ms.author: joshuapa
manager: jillfra
ms.custom: seodec18
ms.workload:
- python
- data-science
ms.openlocfilehash: bf503cff7d8de2c00a93385113de05de00059390
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60112237"
---
# <a name="use-pylint-to-check-python-code"></a>Python kodunu denetlemek için PyLint kullanma

[PyLint](https://www.pylint.org/), Python kodunda hata olup olmadığını denetler ve desenleri, kodlama iyi Python teşvik eder yaygın olarak kullanılan bir araç Python projeleri için Visual Studio ile tümleşiktir.

## <a name="run-pylint"></a>Spustit pylint

Yeni bir Python projeye sağ tıklayın **Çözüm Gezgini** seçip **Python** > **çalıştırma PyLint**:

![Python projeleri için bağlam menüsünde PyLint komutu](media/code-pylint-command.png)

Bu komutu kullanarak zaten mevcut değilse PyLint etkin ortamınıza yüklemenizi ister.

PyLint uyarıları ve hataları görünür **hata listesi** penceresi:

![PyLint hata listesi](media/code-pylint-error-list.png)

Bir hata çift doğrudan sorunu oluşturulan kaynak koduna götürür.

> [!Tip]
> Bkz: [PyLint başvurusu özellikleri](https://pylint.readthedocs.io/en/latest/technical_reference/features.html) PyLint ayrıntılı bir listesi için çıktı iletilerini.

## <a name="set-pylint-command-line-options"></a>PyLint komut satırı seçeneklerini ayarlama

[Komut satırı seçenekleri](https://pylint.readthedocs.io/en/latest/user_guide/run.html#command-line-options) PyLint belgelerin bölümü aracılığıyla PyLint'ın davranışını denetlemek nasıl açıklar bir *.pylintrc* yapılandırma dosyası. Böyle bir dosya Visual Studio'da veya başka bir yerde uygulanan bu ayarlar ne ölçüde istediğinize bağlı olarak Python proje kökündeki yerleştirilebilir (bkz [komut satırı seçenekleri](https://pylint.readthedocs.io/en/latest/user_guide/run.html#command-line-options) Ayrıntılar için).

Örneğin, önceki resimle gösterilen "docstring eksik" uyarıları bastırmak için bir *.pylintrc* dosya bir proje, adımları uygulayın:

1. Komut satırında, proje kök dizinine gidin (sahip, *.pyproj* dosyası) ve bir derleme dışı bırakılan yapılandırma dosyası oluşturmak için aşağıdaki komutu çalıştırın:

   ```command
   pylint --generate-rcfile > .pylintrc
   ```

1. Visual Studio Çözüm Gezgini'nde projenize sağ tıklayın, **Ekle** > **var olan öğe**, yeni gidin *.pylintrc* dosya, onu seçin ve seçin **Ekle**.

1. Çalışabileceğiniz birçok ayarları olan düzenleme için dosyayı açın. Bir uyarıyı devre dışı bırakmak için bulun `[MESSAGES CONTROL]` bölümüne ve ardından bulun `disable` Bu bölümde ayarlama. Belirli iletileri için istediğiniz hangi uyarıların ekleyebilir, uzun bir dizenin yoktur. Örnekte, ekleme `,missing-docstring` (ayırıcı virgül dahil).

1. Kaydet *.pylintrc* dosya ve Uyarıları artık bastırılan yeniden görmek için spustit pylint.

> [!Tip]
> Kullanılacak bir *.pylintrc* adlı bir ortam değişkeni oluşturun, bir ağ paylaşımından dosya `PYLINTRC` ağ üzerinde dosya adı değerine sahip bir UNC yolu veya eşlenen sürücü harfini kullanarak paylaşın. Örneğin: `PYLINTRC=\\myshare\python\.pylintrc`
