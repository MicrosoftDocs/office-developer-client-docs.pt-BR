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
ms.openlocfilehash: 4f5d6a5d2dbb48a86363896bf14b61ed28118330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422660"
---
# <a name="mapi-interfaces"></a><span data-ttu-id="6a25b-103">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="6a25b-103">MAPI Interfaces</span></span>

  
  
<span data-ttu-id="6a25b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a25b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a25b-105">A documentação de cada interface consiste em uma seção introdutória que inclui uma breve descrição da finalidade da interface, seguida de uma tabela que contém as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a25b-105">The documentation for each interface consists of an introductory section that includes a brief description of the interface's purpose followed by a table that contains the following information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a25b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6a25b-106">Header file:</span></span>  <br/> |<span data-ttu-id="6a25b-107">O arquivo de header em que a interface está definida e que deve ser incluído ao compilar o código-fonte.</span><span class="sxs-lookup"><span data-stu-id="6a25b-107">The header file where the interface is defined and that must be included when you compile your source code.</span></span>  <br/> |
|<span data-ttu-id="6a25b-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="6a25b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="6a25b-109">O objeto que expõe a interface.</span><span class="sxs-lookup"><span data-stu-id="6a25b-109">The object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="6a25b-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6a25b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="6a25b-111">Uma lista dos componentes que fornecem uma implementação da interface.</span><span class="sxs-lookup"><span data-stu-id="6a25b-111">A list of the components that provide an implementation of the interface.</span></span>  <br/> |
|<span data-ttu-id="6a25b-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="6a25b-112">Called by:</span></span>  <br/> |<span data-ttu-id="6a25b-113">Uma lista dos componentes que normalmente chamam os métodos da interface.</span><span class="sxs-lookup"><span data-stu-id="6a25b-113">A list of the components that typically call the methods of the interface.</span></span>  <br/> |
|<span data-ttu-id="6a25b-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="6a25b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6a25b-115">O GUID do identificador da interface.</span><span class="sxs-lookup"><span data-stu-id="6a25b-115">The interface identifier GUID.</span></span>  <br/> |
|<span data-ttu-id="6a25b-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="6a25b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="6a25b-117">O tipo de ponteiro para o objeto que expõe a interface.</span><span class="sxs-lookup"><span data-stu-id="6a25b-117">The pointer type for the object that exposes the interface.</span></span>  <br/> |
|<span data-ttu-id="6a25b-118">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="6a25b-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="6a25b-119">Para interfaces derivadas de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="6a25b-119">For interfaces derived from [IMAPIProp](imapipropiunknown.md).</span></span> <span data-ttu-id="6a25b-120">Se não for traduzida, as alterações vigorarão imediatamente; se transacionado, as alterações não são efetivadas até [que IMAPIProp::SaveChanges](imapiprop-savechanges.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="6a25b-120">If nontransacted, changes take effect immediately; if transacted, changes do not take effect until [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span>  <br/> |
   
<span data-ttu-id="6a25b-121">Após a primeira tabela, há outra tabela que lista todos os métodos dessa interface em ordem vtable.</span><span class="sxs-lookup"><span data-stu-id="6a25b-121">Following the first table is another table that lists all the methods of this interface in vtable order.</span></span> <span data-ttu-id="6a25b-122">Uma vtable é uma matriz de ponteiros de função criada pelo compilador contendo um ponteiro de função para cada método de um objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="6a25b-122">A vtable is an array of function pointers created by the compiler containing one function pointer for each method of a MAPI object.</span></span> <span data-ttu-id="6a25b-123">Os métodos são listados na mesma ordem em que são declarados.</span><span class="sxs-lookup"><span data-stu-id="6a25b-123">The methods are listed in the same order that they are declared.</span></span> <span data-ttu-id="6a25b-124">Os métodos herdados de outras interfaces não são mostrados na tabela Ordem da Tabela Vtable, mas podem ser usados da mesma maneira que documentados na interface que os define.</span><span class="sxs-lookup"><span data-stu-id="6a25b-124">Methods inherited from other interfaces are not shown in the Vtable Order table but can be used in the same way as documented in the interface that defines them.</span></span>
  
<span data-ttu-id="6a25b-125">Após cada tópico da interface, os métodos da interface são documentados em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="6a25b-125">After each interface topic, the interface's methods are then documented in alphabetical order.</span></span> <span data-ttu-id="6a25b-126">Para cada método, a documentação inclui uma breve instrução de finalidade, um bloco de sintaxe e as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a25b-126">For each method, the documentation includes a brief purpose statement, a syntax block, and the following information.</span></span>
  
|<span data-ttu-id="6a25b-127">**Título**</span><span class="sxs-lookup"><span data-stu-id="6a25b-127">**Heading**</span></span>|<span data-ttu-id="6a25b-128">**Conteúdo**</span><span class="sxs-lookup"><span data-stu-id="6a25b-128">**Content**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6a25b-129">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a25b-129">Parameters</span></span>  <br/> |<span data-ttu-id="6a25b-130">Uma descrição de cada parâmetro no método.</span><span class="sxs-lookup"><span data-stu-id="6a25b-130">A description of each parameter in the method.</span></span>  <br/> |
|<span data-ttu-id="6a25b-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6a25b-131">Return Value</span></span>  <br/> |<span data-ttu-id="6a25b-132">Uma descrição dos valores exclusivos que o método pode retornar.</span><span class="sxs-lookup"><span data-stu-id="6a25b-132">A description of the unique values that the method can return.</span></span> <span data-ttu-id="6a25b-133">Esses são os valores que os chamadores devem verificar em seu código.</span><span class="sxs-lookup"><span data-stu-id="6a25b-133">These are the values that callers should check for in their code.</span></span>  <br/> |
|<span data-ttu-id="6a25b-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a25b-134">Remarks</span></span>  <br/> |<span data-ttu-id="6a25b-135">Uma descrição do motivo e de como o método é usado.</span><span class="sxs-lookup"><span data-stu-id="6a25b-135">A description of why and how the method is used.</span></span>  <br/> |
|<span data-ttu-id="6a25b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a25b-136">See Also</span></span>  <br/> |<span data-ttu-id="6a25b-137">Referências cruzadas a outros tópicos nesta referência.</span><span class="sxs-lookup"><span data-stu-id="6a25b-137">Cross-references to other topics in this Reference.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a25b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a25b-138">See also</span></span>



[<span data-ttu-id="6a25b-139">Referencia MAPI</span><span class="sxs-lookup"><span data-stu-id="6a25b-139">MAPI Reference</span></span>](mapi-reference.md)

