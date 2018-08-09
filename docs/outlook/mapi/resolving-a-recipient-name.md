---
title: Resolver o nome de um destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 256412f6ccbe66da067411bf9f66ad0478cf5ca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770253"
---
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="a1b70-103">Resolver o nome de um destinatário</span><span class="sxs-lookup"><span data-stu-id="a1b70-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="a1b70-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a1b70-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a1b70-105">Quando uma mensagem é encaminhada, uma lista de destinatários é criada com propriedades relacionadas a cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="a1b70-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="a1b70-106">No momento em que a mensagem é enviada, uma dessas propriedades deve ser um identificador de entrada a longo prazo do destinatário.</span><span class="sxs-lookup"><span data-stu-id="a1b70-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="a1b70-107">Para garantir que cada destinatário inclui a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), passe a estrutura [ADRLIST](adrlist.md) descrevendo sua lista de destinatários no conteúdo do parâmetro _lpAdrList_ em uma chamada para [IAddrBook:: ResolveName](iaddrbook-resolvename.md).</span><span class="sxs-lookup"><span data-stu-id="a1b70-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="a1b70-108">**ResolveName** inicialmente processamento, ignorando as entradas na estrutura de **ADRLIST** que já foram resolvidas, conforme indicado pela presença de um identificador de entrada no correspondente da estrutura [ADRENTRY](adrentry.md) **SPropValue** matriz.</span><span class="sxs-lookup"><span data-stu-id="a1b70-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="a1b70-109">Em seguida, **ResolveName** atribuirá automaticamente identificadores de entrada únicos a dois tipos de destinatários:</span><span class="sxs-lookup"><span data-stu-id="a1b70-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="a1b70-110">Destinatários com um endereço formatado como um endereço de Internet</span><span class="sxs-lookup"><span data-stu-id="a1b70-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="a1b70-111">Destinatários com um endereço formatado como se segue:</span><span class="sxs-lookup"><span data-stu-id="a1b70-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="a1b70-112">Para todas as entradas restantes, **ResolveName** procura o catálogo de endereços uma correspondência exata no nome para exibição.</span><span class="sxs-lookup"><span data-stu-id="a1b70-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="a1b70-113">**ResolveName** usa a propriedade **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) para determinar o conjunto de contêineres a pesquisa e a ordem de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a1b70-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="a1b70-114">O método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) de cada contêiner para tentar resolver todos os nomes de chamadas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="a1b70-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="a1b70-115">Porque alguns contêineres não suportam **ResolveNames**, se o contêiner retornará MAPI_E_NO_SUPPORT, MAPI aplica uma restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) em relação à tabela seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a1b70-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="a1b70-116">Todos os contêineres do catálogo de endereços são necessários para dar suporte a resolução de nomes com essa restrição.</span><span class="sxs-lookup"><span data-stu-id="a1b70-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="a1b70-117">Depois que todos os nomes forem resolvidos, nenhuma outra são feitas chamadas do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a1b70-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="a1b70-118">Se todos os contêineres tiverem sido chamados, mas nomes ambíguos ou não resolvidos permanecerão, MAPI exibe uma caixa de diálogo se possível para solicitar ao usuário para resolver os nomes restantes.</span><span class="sxs-lookup"><span data-stu-id="a1b70-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="a1b70-119">A restrição de **PR_ANR** corresponde ao valor da propriedade **PR_ANR** contra o nome para exibição na estrutura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="a1b70-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="a1b70-120">Limitando a exibição da tabela de conteúdo de um contêiner com a restrição de propriedade **PR_ANR** faz com que o provedor de catálogo de endereços executar um tipo de "melhor adivinhar" da pesquisa, correspondência contra a propriedade que faz sentido para o provedor.</span><span class="sxs-lookup"><span data-stu-id="a1b70-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="a1b70-121">Por exemplo, um provedor de catálogo de endereços sempre pode corresponder nomes na lista de destinatários contra **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) enquanto outra pode permitir que um administrador selecionar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="a1b70-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="a1b70-122">**Para definir uma restrição de propriedade PR_ANR na tabela de conteúdo de um contêiner catálogo de endereços**</span><span class="sxs-lookup"><span data-stu-id="a1b70-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="a1b70-123">Crie uma estrutura [SRestriction](srestriction.md) , conforme mostrado no seguinte código:</span><span class="sxs-lookup"><span data-stu-id="a1b70-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="a1b70-124">Chame o conteúdo [IMAPITable:: Restrict](imapitable-restrict.md) método da tabela, passando a estrutura **SRestriction** como o parâmetro _lpRestriction_ .</span><span class="sxs-lookup"><span data-stu-id="a1b70-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    

