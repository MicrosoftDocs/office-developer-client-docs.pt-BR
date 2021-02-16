---
title: Implementando uma tabela de One-Off contêiner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417417"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="ca429-103">Implementando uma tabela de One-Off contêiner</span><span class="sxs-lookup"><span data-stu-id="ca429-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="ca429-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca429-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca429-105">Para acessar a tabela única pertencente a um de seus contêineres, o MAPI chama o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) com a interface **IMAPITable.**</span><span class="sxs-lookup"><span data-stu-id="ca429-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="ca429-106">Seu contêiner é solicitado a retornar sua tabela única quando um aplicativo cliente está tentando adicionar um destinatário ao contêiner.</span><span class="sxs-lookup"><span data-stu-id="ca429-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="ca429-107">Se o contêiner permitir qualquer destinatário, o provedor poderá retornar sua própria implementação de tabela ou chamar [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) para retornar a implementação de MAPI.</span><span class="sxs-lookup"><span data-stu-id="ca429-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="ca429-108">O conjunto de modelos na tabela única do contêiner deve refletir o tipo de destinatários que o contêiner específico pode conter.</span><span class="sxs-lookup"><span data-stu-id="ca429-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="ca429-109">Normalmente, isso inclui um ou dois modelos, modelos para criar um usuário de mensagens individual ou uma lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="ca429-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="ca429-110">Os identificadores de entrada para esses modelos são mantidos nas propriedades **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) e **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ca429-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="ca429-111">No entanto, os contêineres não são limitados de forma alguma a esses tipos de entradas.</span><span class="sxs-lookup"><span data-stu-id="ca429-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="ca429-112">Eles podem conter outros tipos de destinatários ou entradas que não são de destinatário, como diretórios.</span><span class="sxs-lookup"><span data-stu-id="ca429-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

