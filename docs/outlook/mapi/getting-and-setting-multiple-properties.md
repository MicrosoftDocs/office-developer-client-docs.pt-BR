---
title: Obter e configurar várias propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: dd25751978eb036531238e6372e35934b3ec145a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432258"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="8a5b2-103">Obter e configurar várias propriedades</span><span class="sxs-lookup"><span data-stu-id="8a5b2-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="8a5b2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a5b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a5b2-105">Ao obter e definir o máximo de propriedades possível com o menor número de chamadas, a atividade remota é curtailed e a sobrecarga envolvida com cada propriedade é reduzida.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="8a5b2-106">Embora os provedores de serviços tentem coletar as propriedades antes de fazer uma chamada de procedimento remoto para recuperação ou modificação, você pode otimizar esse esforço solicitando várias propriedades para começar.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="8a5b2-107">Por exemplo, se você trabalhar com listas de roteamento que descrevem destinatários futuros com propriedades nomeadas pertencentes a determinados conjuntos de propriedades, processe todos os destinatários com duas chamadas.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="8a5b2-108">Use uma chamada para [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para recuperar os identificadores de todas as propriedades de destinatário e a outra chamada para [IMAPIProp::](imapiprop-getprops.md) GetProps para recuperar todos os valores.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="8a5b2-109">A alternativa, fazendo uma chamada para **GetIDsFromNames** seguida de uma chamada para \*\*\*\* GetProps para cada destinatário, é muito menos eficiente.</span><span class="sxs-lookup"><span data-stu-id="8a5b2-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

