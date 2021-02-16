---
title: Restrições do Address Book
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7419c174c1f68653794c2dbd836577e8dd3e596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432797"
---
# <a name="address-book-restrictions"></a><span data-ttu-id="91e5c-103">Restrições do Address Book</span><span class="sxs-lookup"><span data-stu-id="91e5c-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="91e5c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91e5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91e5c-105">Os provedores de agendas são necessários para dar suporte a três tipos de restrições nos índices de conteúdo de seus contêineres:</span><span class="sxs-lookup"><span data-stu-id="91e5c-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="91e5c-106">Restrições de propriedade de nome ambíguo</span><span class="sxs-lookup"><span data-stu-id="91e5c-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="91e5c-107">Restrições de propriedade de chave de instância</span><span class="sxs-lookup"><span data-stu-id="91e5c-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="91e5c-108">Restrições de conteúdo de nome de exibição prefixados</span><span class="sxs-lookup"><span data-stu-id="91e5c-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="91e5c-109">Restrições de nome ambíguas são restrições de propriedade usando a **propriedade PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para corresponder nomes de destinatários com entradas em contêineres de livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="91e5c-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="91e5c-110">A **PR_ANR** restrição de propriedade é um tipo de "melhor suposição" de pesquisa pelo qual os provedores de agendas de endereços podem escolher a propriedade correspondente que funciona melhor para seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="91e5c-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="91e5c-111">Por exemplo, um provedor de agendas de endereços pode implementar PR_ANR restrição correspondendo **nomes** de **destinatários** à propriedade PR_ACCOUNT ([PidTagAccount](pidtagaccount-canonical-property.md)) de cada entrada de contêiner, enquanto outro provedor pode usar **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="91e5c-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="91e5c-112">O MAPI recomenda que as implementações da restrição **de PR_ANR** equilibrem entre o desempenho adequado e a satisfação do usuário.</span><span class="sxs-lookup"><span data-stu-id="91e5c-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="91e5c-113">A satisfação do usuário pode ser comprometida quando um provedor de agendas implementa a restrição de forma que muitas ou muitas combinações sejam encontradas.</span><span class="sxs-lookup"><span data-stu-id="91e5c-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="91e5c-114">Alguns provedores de agendas de endereço suportam o que é conhecido como um nome distinto, ou comum, que não é exibido em uma caixa de diálogo, mas pode corresponder a uma restrição de nome ambígua.</span><span class="sxs-lookup"><span data-stu-id="91e5c-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="91e5c-115">Uma implementação típica pode ser analisar o nome de exibição do destinatário em palavras, correspondendo a qualquer entrada que contenha todas as palavras.</span><span class="sxs-lookup"><span data-stu-id="91e5c-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="91e5c-116">Atenção aos detalhes, como sensibilidade à posição da palavra, se palavras não seguras são acionadas e a escolha de caracteres separadores pode variar.</span><span class="sxs-lookup"><span data-stu-id="91e5c-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="91e5c-117">Por exemplo, se o nome a ser resolvido  for "Bill L", uma restrição PR_ANR comum selecionará as seguintes entradas como correspondentes:</span><span class="sxs-lookup"><span data-stu-id="91e5c-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="91e5c-118">Dra.</span><span class="sxs-lookup"><span data-stu-id="91e5c-118">Billy Larson</span></span>
    
- <span data-ttu-id="91e5c-119">Bill Lee</span><span class="sxs-lookup"><span data-stu-id="91e5c-119">Bill Lee</span></span>
    
- <span data-ttu-id="91e5c-120">Bill Logan Jr.</span><span class="sxs-lookup"><span data-stu-id="91e5c-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="91e5c-121">Sam Bill Lee</span><span class="sxs-lookup"><span data-stu-id="91e5c-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="91e5c-122">Restrições de chave de instância ou **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) são usadas na implementação de caixas de listagem que são usadas em aplicativos cliente para exibir tabelas MAPI.</span><span class="sxs-lookup"><span data-stu-id="91e5c-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="91e5c-123">Algumas implementações de caixa de listagem permitem que os usuários façam várias seleções, rolem para cima ou para baixo e retornem ao primeiro item selecionado.</span><span class="sxs-lookup"><span data-stu-id="91e5c-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="91e5c-124">Para implementar esse comportamento, os clientes chamam [IMAPITable::FindRow](imapitable-findrow.md), passando uma restrição de propriedade na propriedade **PR_INSTANCE_KEY** para o método.</span><span class="sxs-lookup"><span data-stu-id="91e5c-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="91e5c-125">Os provedores de agendas são necessários para dar suporte a essa restrição.</span><span class="sxs-lookup"><span data-stu-id="91e5c-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="91e5c-126">Outro recurso de caixas de listagem usadas para exibição de tabela é a capacidade de posicionar o cursor com base em um conjunto de caracteres de prefixo.</span><span class="sxs-lookup"><span data-stu-id="91e5c-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="91e5c-127">À medida que o usuário começa a digitar caracteres de prefixo, o cliente move o cursor para o primeiro item que começa com esses caracteres.</span><span class="sxs-lookup"><span data-stu-id="91e5c-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="91e5c-128">Os clientes implementam esse recurso com uma restrição de conteúdo com **base na propriedade PR_DISPLAY_NAME** e no nível FL_PREFIX difusa.</span><span class="sxs-lookup"><span data-stu-id="91e5c-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="91e5c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="91e5c-129">See also</span></span>



[<span data-ttu-id="91e5c-130">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="91e5c-130">MAPI Tables</span></span>](mapi-tables.md)

