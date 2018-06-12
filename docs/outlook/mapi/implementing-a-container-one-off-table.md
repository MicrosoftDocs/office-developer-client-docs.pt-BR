---
title: Implementando uma tabela de contêiner únicos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 83351e18750ccbffbe60c4e19f9b04a9c94a42e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767401"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="187e6-103">Implementando uma tabela de contêiner únicos</span><span class="sxs-lookup"><span data-stu-id="187e6-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="187e6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="187e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="187e6-105">Para acessar a tabela único pertencente a um dos seus contêineres, MAPI chama o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) com o **IMAPITable** interface.</span><span class="sxs-lookup"><span data-stu-id="187e6-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="187e6-106">Seu contêiner é solicitado para retornar sua tabela único quando um aplicativo cliente está tentando adicionar um destinatário para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="187e6-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="187e6-107">Se o contêiner permite quaisquer destinatários, seu provedor pode retornar sua própria implementação de tabela ou chamada [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) para retornar a implementação de MAPI.</span><span class="sxs-lookup"><span data-stu-id="187e6-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="187e6-108">O conjunto de modelos na tabela únicos contêiner deve refletir o tipo de destinatários que pode conter no contêiner específico.</span><span class="sxs-lookup"><span data-stu-id="187e6-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="187e6-109">Normalmente, isso inclui um ou dois modelos, modelos para a criação de um usuário individual de mensagens ou uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="187e6-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="187e6-110">Os identificadores de entrada para esses modelos são mantidos no **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) e propriedades de **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="187e6-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="187e6-111">No entanto, os contêineres a intenção não estão limitados a esses tipos de entradas.</span><span class="sxs-lookup"><span data-stu-id="187e6-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="187e6-112">Eles podem conter outros tipos de destinatários ou entradas de não-recipient como diretórios.</span><span class="sxs-lookup"><span data-stu-id="187e6-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

