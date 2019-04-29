---
title: Resolver o nome de um destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405861"
---
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="85122-103">Resolver o nome de um destinatário</span><span class="sxs-lookup"><span data-stu-id="85122-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="85122-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85122-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85122-105">Quando uma mensagem é endereçada, uma lista de destinatários é criada com propriedades relacionadas a cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="85122-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="85122-106">No momento em que a mensagem é enviada, uma dessas propriedades deve ser o identificador de entrada de longo prazo do destinatário.</span><span class="sxs-lookup"><span data-stu-id="85122-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="85122-107">Para garantir que cada destinatário inclua a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), passe a estrutura [das ADRLIST](adrlist.md) descrevendo sua lista de destinatários no conteúdo do parâmetro _lpAdrList_ em uma chamada para [IAddrBook:: ResolveName](iaddrbook-resolvename.md).</span><span class="sxs-lookup"><span data-stu-id="85122-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="85122-108">\*\*\*\* O resolvedor começa o processamento, ignorando as entradas na estrutura **das ADRLIST** que já foram resolvidas, conforme indicado pela presença de um identificador de entrada no **SPropValue** da estrutura [ADRENTRY](adrentry.md) correspondente Storage.</span><span class="sxs-lookup"><span data-stu-id="85122-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="85122-109">Em seguida \*\*\*\* , ResolveName atribui automaticamente identificadores de entrada únicos a dois tipos de destinatários:</span><span class="sxs-lookup"><span data-stu-id="85122-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="85122-110">Destinatários com um endereço formatado como um endereço da Internet</span><span class="sxs-lookup"><span data-stu-id="85122-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="85122-111">Destinatários com um endereço formatado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="85122-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="85122-112">Para todas as entradas restantes \*\*\*\* , ResolveName procura no catálogo de endereços uma correspondência exata no nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="85122-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="85122-113">\*\*\*\* O resolvedor usa a propriedade **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) para determinar o conjunto de contêineres a ser pesquisado e a ordem de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="85122-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="85122-114">MAPI chama o método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) de todos os contêineres para tentar resolver todos os nomes.</span><span class="sxs-lookup"><span data-stu-id="85122-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="85122-115">Como alguns contêineres não oferecem \*\*\*\* suporte a ResolveNames, se o contêiner retornar MAPI_E_NO_SUPPORT, MAPI aplica uma restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) em relação a sua tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="85122-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="85122-116">Todos os contêineres do catálogo de endereços são necessários para dar suporte à resolução de nomes com essa restrição.</span><span class="sxs-lookup"><span data-stu-id="85122-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="85122-117">Depois que todos os nomes forem resolvidos, não serão feitas outras chamadas de contêiner.</span><span class="sxs-lookup"><span data-stu-id="85122-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="85122-118">Se todos os contêineres tiverem sido chamados, mas os nomes ambíguos ou não resolvidos permanecerem, MAPI exibirá uma caixa de diálogo, se possível, para solicitar que o usuário resolva os nomes restantes.</span><span class="sxs-lookup"><span data-stu-id="85122-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="85122-119">A restrição **PR_ANR** corresponde ao valor da propriedade **PR_ANR** em relação ao nome de exibição na estrutura **das ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="85122-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="85122-120">Limitar o modo de exibição da tabela de conteúdo de um contêiner com a restrição de propriedade **PR_ANR** faz com que o provedor de catálogo de endereços execute um tipo de pesquisa de melhor adivinhação, correspondendo à propriedade que faz sentido para o provedor.</span><span class="sxs-lookup"><span data-stu-id="85122-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="85122-121">Por exemplo, um provedor de catálogo de endereços sempre pode coincidir nomes na lista de destinatários em relação ao **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), enquanto outro pode permitir que um administrador selecione a propriedade.</span><span class="sxs-lookup"><span data-stu-id="85122-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="85122-122">**Para definir uma restrição de propriedade PR_ANR em uma tabela de conteúdo do contêiner de catálogo de endereços**</span><span class="sxs-lookup"><span data-stu-id="85122-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="85122-123">Crie uma estrutura [SRestriction](srestriction.md) conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="85122-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="85122-124">Chame o método imApitable [:: Restrict](imapitable-restrict.md) da tabela de conteúdo, passando a estrutura **SRestriction** como o parâmetro _lpRestriction_ .</span><span class="sxs-lookup"><span data-stu-id="85122-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    

