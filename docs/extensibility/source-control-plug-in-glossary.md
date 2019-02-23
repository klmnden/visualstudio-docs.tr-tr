---
title: Kaynak Denetimi Eklentisi sözlüğü | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- glossary [Visual Studio SDK]
- source control plug-ins, glossary
ms.assetid: f224bbc9-38fc-4c80-ab09-51dcc8969f8e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0df624a27513fa0eb18b2643bb7c680d71d94c0c
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56722382"
---
# <a name="source-control-plug-in-glossary"></a>Kaynak Denetimi Eklentisi Sözlüğü
Aşağıdaki yardımcı terimleri ve tanımları kaynak denetimi eklentisi SDK belgelerine ilgilidir.

## <a name="definitions"></a>Tanımlar
 Bir kullanıcı için bir çalışma kopyası değişiklik yapıldığında iade etme, bir kullanıcı, merkezi kaynak denetim deposu ile çalışma kopyadan değişiklikleri göndermeniz gerekir. Bu, diğer kullanıcılar için kullanılabilir olan dosyayı yeni bir düzeltmesi oluşturulur. Bu işlem, bir iade etme denir.

 Kullanıma alma çalışma kopyası amacınızla değiştirmek için depoyu bildiren depodan isteme işlemi. Bir çalışan kopya kullanıma andan itibaren proje durumunu yansıtır.

 Kaynak kodu denetim sistemi kullanan bir istemci programı. Bu belgede, bu Visual Studio IDE olur.

 Kaynak denetimi işlemi gerçekleştirilirken bir kullanıcı için bir düzeltme ekleyebilirsiniz değişiklikleri açıklayan bir yorum ileti.

 Aynı dosyanın aynı bölgeye iki kullanıcılar iade etmeyi denediğinde bir çakışma durumu değişir. Genellikle, bir birleştirme gerçekleştirilmelidir.

 Dizin bir istemci-tarafı yerel klasörü dizin olarak adlandırılır. Bu, bir kullanıcının değişiklikleri gerçekten yaptığı kopyasıdır. Belirli bir projenin birçok çalışma kopyalarının olabilir; genellikle her geliştirici kendi kopya vardır.

 Get bir Al işlemi, kullanıcının çalışma kopyası güncel depo kopyalama ile getirir. Kullanıcı yalnızca en son kopyasını gerekiyor ancak değişiklik amaçlayan bir kullanıma alma, bir get gerçekleştirilir.

 Genellikle tüm kullanıma alma, iadeler, güncelleştirmeleri, etiketler ve kaynak denetim deposunda bitti yayınlar özetini olan geçmiş.

 Genelde IDE, Visual Studio tümleşik geliştirme ortamına anlamına gelir. Ancak, kaynak denetimi eklentisi API tanımak diğer istemci ortamları da başvurabileceğiniz.

 İşlem sırasında hangi iki veya daha fazla kaynak kod dosyaları önceki dosyalarından tüm özellikleri içerir, yeni bir dosya oluşturmak üzere birleştirilir birleştirin. Bu kavramı burada iki veya daha fazla geliştiriciler dosyalar üzerinde eşzamanlı olarak çalışabilir sürüm denetiminde önemlidir.

 Bir proje kaynak denetimi klasörü, genellikle bir proje olarak da adlandırılır. Visual Studio'da bu projeler veya çözümler ile hiçbir ilişkisi yok.

 Kaynak Denetimi Eklentisi API uygulayarak kaynak denetimi işlevlerini sağlar. eklentisini bir DLL.

 Bir kaynak denetim sistemi bir projenin tam düzeltme geçmişi depoladığı ana kopya deposu. Her projenin tam olarak bir depo yok.

 Bir dosyanın geçmişini veya dosya kümesini değişiklik düzeltme bir taahhüt. Bir düzeltme biridir sürekli olarak değişen bir projede anlık görüntüsünü alın.

## <a name="see-also"></a>Ayrıca Bkz.
- [Kaynak Denetimi Eklentileri](../extensibility/source-control-plug-ins.md)