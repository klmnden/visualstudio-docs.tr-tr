---
title: Node.js REPL kullanma
description: Visual Studio Node.js çalışma zamanı ile etkileşim kurmaya yönelik destek sağlar.
ms.custom: ''
ms.date: 12/04/2018
ms.technology: vs-nodejs
ms.topic: conceptual
ms.devlang: javascript
author: mikejo5000
ms.author: mikejo
manager: douge
dev_langs:
- JavaScript
ms.workload:
- nodejs
ms.openlocfilehash: 7b980634a95c14413dd07649893a26b21de6f78d
ms.sourcegitcommit: a715de2ba8c703f37aa2102567b1aa2c0f05a117
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/15/2018
ms.locfileid: "53443346"
---
# <a name="work-with-the-nodejs-interactive-window"></a>Node.js etkileşimli penceresi ile çalışma

Visual Studio için node.js araçları yüklü Node.js çalışma zamanı için etkileşimli bir pencere içerir. Bu pencere, JavaScript kodu girin ve sonuçları hemen görmenize yanı sıra geçerli proje ile etkileşim kurmak için npm komutları yürütmek sağlar. Etkileşimli olarak da bilinen REPL penceresidir (**R**okunur /**E**valuate /**P**azdır **L**oop).

## <a name="open-the-interactive-window"></a>Etkileşimli penceresini açın

Etkileşimli pencere, Çözüm Gezgini'nde Node.js proje düğümünü sağ tıklatıp seçerek açabilirsiniz **Node.js etkileşimli penceresini aç**.

![Node.js etkileşimli pencerede proje bağlam menüsü](../javascript/media/interactivewindow-open-from-project.png)

Node.js etkileşimli penceresi açmak için varsayılan kısayol tuşları **[CTRL] + K, N**. Veya araç penceresini seçerek açabilirsiniz **görünümü** > **Windows** > **Node.js etkileşimli penceresi**.

## <a name="use-the-repl"></a>REPL kullanma

Açılan sonra komutları girebilirsiniz.

![Node.js etkileşimli penceresi](../javascript/media/interactivewindow.png)

Etkileşimli pencere, bildirdiğiniz herhangi bir JavaScript işlevinden bunları ayırt etmek için bir nokta önek ile başlayan birkaç yerleşik komutlar vardır. Aşağıdaki komutlar desteklenir:

**.CLS, .clear** Düzenleyicisi penceresinin geçmiş ve yürütme bağlamı dokunmadan, içeriği temizler.

**.Help** belirtilmezse Yardım belirtilen komut ya da tüm kullanılabilir komutları ve tuş bağlamaları'görüntüler.

**.info** kullanılan geçerli Node.js hakkında bilgi yürütülebilir gösterir getirin.

**.npm** npm komutunu çalıştırır. Çözüm birden fazla proje içeriyorsa, kullanarak hedef projeyi belirtin `.npm [projectname] <npm arguments>`.

**.reset** yürütme ortamını ilk durumuna, Canlı geçmişi sıfırlar.

**.Save** geçerli REPL oturumunu bir dosyaya kaydeder.