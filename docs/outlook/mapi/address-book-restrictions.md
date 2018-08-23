---
title: Restrições de catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 54cd90cac6c00e8cf274e0b78a1bfec32401bb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576509"
---
# <a name="address-book-restrictions"></a><span data-ttu-id="23f8f-103">Restrições de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="23f8f-103">Address Book Restrictions</span></span>

  
  
<span data-ttu-id="23f8f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23f8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23f8f-105">Provedores de catálogo de endereços são necessários para oferecer suporte a três tipos de restrições nos índices de conteúdo de seus contêineres:</span><span class="sxs-lookup"><span data-stu-id="23f8f-105">Address book providers are required to support three types of restrictions on the contents tables of their containers:</span></span>
  
- <span data-ttu-id="23f8f-106">Restrições de propriedade de nome ambígua</span><span class="sxs-lookup"><span data-stu-id="23f8f-106">Ambiguous name property restrictions</span></span>
    
- <span data-ttu-id="23f8f-107">Restrições de propriedade de chave de instância</span><span class="sxs-lookup"><span data-stu-id="23f8f-107">Instance key property restrictions</span></span>
    
- <span data-ttu-id="23f8f-108">Restrições de conteúdo de nome de exibição de prefixo</span><span class="sxs-lookup"><span data-stu-id="23f8f-108">Prefixed display name content restrictions</span></span>
    
<span data-ttu-id="23f8f-109">Restrições de nome ambígua são restrições de propriedade usando a propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) para corresponder os nomes dos destinatários com entradas nos contêineres de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="23f8f-109">Ambiguous name restrictions are property restrictions using the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property to match recipient names with entries in address book containers.</span></span> <span data-ttu-id="23f8f-110">A restrição de propriedade **PR_ANR** é um tipo de "melhor adivinhar" da pesquisa na qual provedores do catálogo de endereços podem escolher a propriedade correspondente que funciona melhor para seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="23f8f-110">The **PR_ANR** property restriction is a "best guess" type of search whereby address book providers can choose the matching property that works best for their container.</span></span> <span data-ttu-id="23f8f-111">Por exemplo, um provedor de catálogo de endereços pode implementar a restrição **PR_ANR** por nomes de destinatário correspondentes contra a propriedade **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) de cada entrada de contêiner enquanto outro provedor pode usar **PR_DISPLAY _NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="23f8f-111">For example, one address book provider might implement the **PR_ANR** restriction by matching recipient names against the **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) property of each container entry whereas another provider might use **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span></span>
  
<span data-ttu-id="23f8f-112">MAPI recomenda que implementações da restrição **PR_ANR** obter um equilíbrio entre desempenho adequado e satisfação do usuário.</span><span class="sxs-lookup"><span data-stu-id="23f8f-112">MAPI recommends that implementations of the **PR_ANR** restriction strike a balance between adequate performance and user satisfaction.</span></span> <span data-ttu-id="23f8f-113">Satisfação do usuário pode ser comprometida quando um provedor de catálogo de endereços implementa a restrição de tal forma que forem encontradas correspondências poucos ou muitos.</span><span class="sxs-lookup"><span data-stu-id="23f8f-113">User satisfaction can be compromised when an address book provider implements the restriction in such a way that too few or too many matches are found.</span></span> <span data-ttu-id="23f8f-114">Suportam para alguns provedores de catálogo de endereços que é conhecido como um nome diferenciado ou comum que não é para exibição em uma caixa de diálogo, mas pode fazer a correspondência de uma restrição de nome ambígua.</span><span class="sxs-lookup"><span data-stu-id="23f8f-114">Some address book providers support what is known as a distinguished, or common, name that is not displayable in a dialog box but can match an ambiguous name restriction.</span></span> 
  
<span data-ttu-id="23f8f-115">Uma implementação típica pode ser para analisar o nome para exibição do destinatário em palavras, a correspondência de qualquer entrada que contém todas as palavras.</span><span class="sxs-lookup"><span data-stu-id="23f8f-115">A typical implementation might be to parse the recipient's display name into words, matching any entry that contains all of the words.</span></span> <span data-ttu-id="23f8f-116">Atenção aos detalhes como a sensibilidade à posição do word, se as palavras não consecutivos são comparadas e a opção de caracteres separadores podem variar.</span><span class="sxs-lookup"><span data-stu-id="23f8f-116">Attention to details such as sensitivity to word position, whether nonconsecutive words are matched, and the choice of separator characters can vary.</span></span> <span data-ttu-id="23f8f-117">Por exemplo, se o nome a ser resolvido for "Bill L", uma restrição de **PR_ANR** típica selecionaria as entradas a seguir como correspondência:</span><span class="sxs-lookup"><span data-stu-id="23f8f-117">For example, if the name to be resolved is "Bill L," a typical **PR_ANR** restriction would select the following entries as matching:</span></span> 
  
- <span data-ttu-id="23f8f-118">Billy Larson</span><span class="sxs-lookup"><span data-stu-id="23f8f-118">Billy Larson</span></span>
    
- <span data-ttu-id="23f8f-119">Bill Lee</span><span class="sxs-lookup"><span data-stu-id="23f8f-119">Bill Lee</span></span>
    
- <span data-ttu-id="23f8f-120">Bill Jr do Logan.</span><span class="sxs-lookup"><span data-stu-id="23f8f-120">Bill Logan Jr.</span></span> 
    
- <span data-ttu-id="23f8f-121">Sam Bill Lee</span><span class="sxs-lookup"><span data-stu-id="23f8f-121">Sam Bill Lee</span></span>
    
<span data-ttu-id="23f8f-122">Restrições de chave de instância ou restrições de propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), são usadas na implementação das caixas de listagem que são usados em aplicativos cliente para exibir as tabelas MAPI.</span><span class="sxs-lookup"><span data-stu-id="23f8f-122">Instance key restrictions, or **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property restrictions, are used in the implementation of list boxes that are used in client applications for viewing MAPI tables.</span></span> <span data-ttu-id="23f8f-123">Algumas implementações de caixa de lista permitem aos usuários fazer várias seleções, rolar para cima ou para baixo e retorno para o primeiro item selecionado.</span><span class="sxs-lookup"><span data-stu-id="23f8f-123">Some list box implementations allow users to make multiple selections, scroll up or down, and return to the first item selected.</span></span> <span data-ttu-id="23f8f-124">Para implementar esse comportamento, clientes [IMAPITable:: FindRow](imapitable-findrow.md), passando uma restrição de propriedade na propriedade **PR_INSTANCE_KEY** para o método de chamada.</span><span class="sxs-lookup"><span data-stu-id="23f8f-124">To implement this behavior, clients call [IMAPITable::FindRow](imapitable-findrow.md), passing a property restriction on the **PR_INSTANCE_KEY** property to the method.</span></span> <span data-ttu-id="23f8f-125">Provedores de catálogo de endereços são necessárias para dar suporte a essa restrição.</span><span class="sxs-lookup"><span data-stu-id="23f8f-125">Address book providers are required to support this restriction.</span></span> 
  
<span data-ttu-id="23f8f-126">Outro recurso das caixas de listagem usado para exibição de tabela é a capacidade para posicionar o cursor com base em um conjunto de caracteres de prefixo.</span><span class="sxs-lookup"><span data-stu-id="23f8f-126">Another feature of list boxes used for table viewing is the ability to position the cursor based on a set of prefix characters.</span></span> <span data-ttu-id="23f8f-127">À medida que o usuário começar a digitar caracteres de prefixo, o cliente move o cursor para o primeiro item começando com esses caracteres.</span><span class="sxs-lookup"><span data-stu-id="23f8f-127">As the user starts typing prefix characters, the client moves the cursor to the first item that begins with these characters.</span></span> <span data-ttu-id="23f8f-128">Clientes implementam esse recurso com uma restrição de conteúdo com base na propriedade **PR_DISPLAY_NAME** e o nível de difusa FL_PREFIX.</span><span class="sxs-lookup"><span data-stu-id="23f8f-128">Clients implement this feature with a content restriction based on the **PR_DISPLAY_NAME** property and the FL_PREFIX fuzzy level.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="23f8f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="23f8f-129">See also</span></span>



[<span data-ttu-id="23f8f-130">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="23f8f-130">MAPI Tables</span></span>](mapi-tables.md)

