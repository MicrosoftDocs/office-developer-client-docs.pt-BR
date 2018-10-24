---
title: Interfaces MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 34a66cf0-b4e0-4fd5-b937-cd157888961d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ca3752e8f7e910994811dec85cc2f1b00e184661
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584804"
---
# <a name="mapi-interfaces"></a><span data-ttu-id="8b081-103">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="8b081-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="8b081-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b081-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b081-105">A documentação para cada interface consiste em uma seção introdutória que inclui uma breve descrição do objetivo da interface seguido de uma tabela que contém as seguintes informações.</span><span class="sxs-lookup"><span data-stu-id="8b081-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b081-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="8b081-106">Header file:</span></span>  <br/> |<span data-ttu-id="8b081-107">O arquivo de cabeçalho onde a interface é definida e que deve ser incluído quando você compila seu código-fonte.</span><span class="sxs-lookup"><span data-stu-id="8b081-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="8b081-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="8b081-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8b081-109">O objeto que expõe a interface.</span><span class="sxs-lookup"><span data-stu-id="8b081-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="8b081-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="8b081-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8b081-111">Uma lista dos componentes que oferecem uma implementação da interface.</span><span class="sxs-lookup"><span data-stu-id="8b081-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="8b081-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="8b081-112">Called by:</span></span>  <br/> |<span data-ttu-id="8b081-113">Uma lista dos componentes que geralmente chame os métodos da interface.</span><span class="sxs-lookup"><span data-stu-id="8b081-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="8b081-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="8b081-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8b081-115">O identificador de interface GUID.</span><span class="sxs-lookup"><span data-stu-id="8b081-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="8b081-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="8b081-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="8b081-117">O tipo de ponteiro para o objeto que expõe a interface.</span><span class="sxs-lookup"><span data-stu-id="8b081-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="8b081-118">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="8b081-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="8b081-119">Para interfaces derivado do [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="8b081-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="8b081-120">Se nontransacted, as alterações entrem em vigor imediatamente; Se transacionadas, as alterações não entrarão em vigor até que [IMAPIProp::SaveChanges](imapiprop-savechanges.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="8b081-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="8b081-121">A primeira tabela a seguir é outra tabela que lista todos os métodos dessa interface na ordem vtable.</span><span class="sxs-lookup"><span data-stu-id="8b081-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="8b081-122">Uma vtable é uma matriz de indicadores de função criado pelo compilador que contém um ponteiro de função para cada método de um objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="8b081-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="8b081-123">Os métodos são listados na mesma ordem em que eles são declarados.</span><span class="sxs-lookup"><span data-stu-id="8b081-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="8b081-124">Métodos herdados de outras interfaces não são mostrados na tabela a ordem Vtable, mas podem ser usados da mesma forma, conforme documentado na interface do que as define.</span><span class="sxs-lookup"><span data-stu-id="8b081-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="8b081-125">Após cada tópico interface, os métodos da interface estão documentados, em seguida, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="8b081-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="8b081-126">Para cada método, a documentação inclui uma instrução de finalidade breve, um bloco de sintaxe e as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b081-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="8b081-127">**Título**</span><span class="sxs-lookup"><span data-stu-id="8b081-127">**Heading**</span></span>|<span data-ttu-id="8b081-128">**Conteúdo**</span><span class="sxs-lookup"><span data-stu-id="8b081-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b081-129">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b081-129">Parameters</span></span>  <br/> |<span data-ttu-id="8b081-130">Uma descrição de cada parâmetro do método.</span><span class="sxs-lookup"><span data-stu-id="8b081-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="8b081-131">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8b081-131">Return Value</span></span>  <br/> |<span data-ttu-id="8b081-132">Uma descrição dos valores exclusivos que o método pode ser retornado.</span><span class="sxs-lookup"><span data-stu-id="8b081-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="8b081-133">Estes são os valores que os chamadores devem verificar se há em seu código.</span><span class="sxs-lookup"><span data-stu-id="8b081-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="8b081-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b081-134">Remarks</span></span>  <br/> |<span data-ttu-id="8b081-135">Uma descrição do porque e como o método é usado.</span><span class="sxs-lookup"><span data-stu-id="8b081-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="8b081-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8b081-136">See Also</span></span>  <br/> |<span data-ttu-id="8b081-137">Referências cruzadas para outros tópicos nesta referência.</span><span class="sxs-lookup"><span data-stu-id="8b081-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8b081-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b081-138">See also</span></span>



[<span data-ttu-id="8b081-139">Refer�ncia MAPI (em ingl�s)</span><span class="sxs-lookup"><span data-stu-id="8b081-139">MAPI Reference</span></span>](mapi-reference.md)

