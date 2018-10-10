---
title: Tipos de cursores (referência de banco de dados da área de trabalho do Access)
TOCTitle: Types of Cursors
ms:assetid: 589f3755-3cf5-9470-bd66-8e8afa218fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249299(v=office.15)
ms:contentKeyID: 48544996
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 559d2ea0ccf1cb34e801d75657695f191ef7076b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462759"
---
# <a name="types-of-cursors"></a><span data-ttu-id="46790-102">Tipos de cursores</span><span class="sxs-lookup"><span data-stu-id="46790-102">Types of Cursors</span></span>


<span data-ttu-id="46790-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="46790-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="46790-p101">Como regra geral, o aplicativo deve usar o cursor mais simples que forneça o acesso a dados necessário. Cada característica adicional do cursor, além das básicas (somente encaminhamento, somente leitura, estático, rolagem, sem buffer) tem um preço  em memória do cliente, em carga ou em desempenho da rede. Em muitos casos, as opções padrão de cursor geram um cursor mais complexo do que a necessidade real do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46790-p101">As a general rule, your application should use the simplest cursor that provides the required data access. Each additional cursor characteristic beyond the basics (forward-only, read-only, static, scrolling, unbuffered) has a price — in client memory, network load, or performance. In many cases, the default cursor options generate a more complex cursor than your application actually needs.</span></span>

<span data-ttu-id="46790-107">A sua escolha do tipo de cursor depende de como o seu aplicativo usa o conjunto de resultados e também de várias considerações sobre design, inclusive o tamanho do conjunto de resultados, a porcentagem de dados com probabilidade de uso, a sensibilidade às alterações dos dados e os requisitos de desempenho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46790-107">Your choice of cursor type depends on how your application uses the result set and also on several design considerations, including the size of the result set, the percentage of the data likely to be used, sensitivity to data changes, and application performance requirements.</span></span>

<span data-ttu-id="46790-108">Na sua forma mais básica, a escolha do cursor depende da sua necessidade de alterar os dados ou apenas de exibi-los:</span><span class="sxs-lookup"><span data-stu-id="46790-108">At its most basic, your cursor choice depends on whether you need to change or simply view the data:</span></span>

  - <span data-ttu-id="46790-109">Se você precisa apenas rolar um conjunto de resultados, sem alterar os dados, use um cursor [somente de encaminhamento](forward-only-cursors.md) ou [estático](static-cursors.md).</span><span class="sxs-lookup"><span data-stu-id="46790-109">If you just need to scroll through a set of results, but not change data, use a [forward-only](forward-only-cursors.md) or [static](static-cursors.md) cursor.</span></span>

  - <span data-ttu-id="46790-110">Se você tiver um grande conjunto de resultados e precisar selecionar apenas algumas linhas, use um cursor de [conjunto de chaves](keyset-cursors.md).</span><span class="sxs-lookup"><span data-stu-id="46790-110">If you have a large result set and need to select just a few rows, use a [keyset](keyset-cursors.md) cursor.</span></span>

  - <span data-ttu-id="46790-111">Se desejar sincronizar um conjunto de resultados com inclusões, alterações e exclusões recentes feitas por todos os usuários atuais, use um cursor [dinâmico](dynamic-cursors.md).</span><span class="sxs-lookup"><span data-stu-id="46790-111">If you want to synchronize a result set with recent adds, changes, and deletes by all concurrent users, use a [dynamic](dynamic-cursors.md) cursor.</span></span>

<span data-ttu-id="46790-112">Embora cada tipo de cursor pareça distinto, lembre-se de que esses tipos não são variedades tão diferentes, mas o simples resultado da sobreposição de características e opções.</span><span class="sxs-lookup"><span data-stu-id="46790-112">Although each cursor type seems to be distinct, keep in mind that these cursor types are not so much different varieties as simply the result of overlapping characteristics and options.</span></span>

