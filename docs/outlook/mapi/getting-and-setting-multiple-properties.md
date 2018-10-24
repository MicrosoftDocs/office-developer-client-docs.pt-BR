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
ms.openlocfilehash: 88c3e0bdb3cc6660e35faf62c5bb63ec2f6352bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590369"
---
# <a name="getting-and-setting-multiple-properties"></a><span data-ttu-id="f882f-103">Obter e configurar várias propriedades</span><span class="sxs-lookup"><span data-stu-id="f882f-103">Getting and setting multiple properties</span></span>

<span data-ttu-id="f882f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f882f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f882f-105">Obtendo e definindo propriedades quantos possíveis com o menor número de chamadas, remotas atividade é curtailed e a sobrecarga envolvida com cada propriedade é reduzida.</span><span class="sxs-lookup"><span data-stu-id="f882f-105">By getting and setting as many properties as possible with the least number of calls, remote activity is curtailed and the overhead involved with each property is reduced.</span></span> <span data-ttu-id="f882f-106">Embora os provedores de serviços tentarem coletar propriedades antes de fazer uma chamada de procedimento remoto para recuperação ou modificação, você pode otimizar desse esforço solicitando-se começar com várias propriedades.</span><span class="sxs-lookup"><span data-stu-id="f882f-106">Although service providers try to collect properties before making a remote procedure call for retrieval or modification, you can optimize this effort by requesting multiple properties to begin with.</span></span>
  
<span data-ttu-id="f882f-107">Por exemplo, se você trabalha com listas de roteamento que descrevem os destinatários futuros com propriedades nomeadas que pertencem aos conjuntos de propriedade específica, processe todos os destinatários com duas chamadas.</span><span class="sxs-lookup"><span data-stu-id="f882f-107">For example, if you work with routing lists that describe future recipients with named properties belonging to particular property sets, process all of the recipients with two calls.</span></span> <span data-ttu-id="f882f-108">Use uma chamada de [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para recuperar os identificadores para todas as propriedades do destinatário e a outra chamada para [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar todos os valores.</span><span class="sxs-lookup"><span data-stu-id="f882f-108">Use one call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to retrieve the identifiers for all of the recipient properties and the other call to [IMAPIProp::GetProps](imapiprop-getprops.md) to retrieve all of the values.</span></span> <span data-ttu-id="f882f-109">A alternativa, fazendo uma chamada para **GetIDsFromNames** seguido por uma chamada para **GetProps** para cada destinatário, é muito menos eficiente.</span><span class="sxs-lookup"><span data-stu-id="f882f-109">The alternative, making a call to **GetIDsFromNames** followed by a call to **GetProps** for each recipient, is much less efficient.</span></span> 
  

