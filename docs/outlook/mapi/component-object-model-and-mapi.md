---
title: COM (Component Object Model) e MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334465"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="984e4-103">COM (Component Object Model) e MAPI</span><span class="sxs-lookup"><span data-stu-id="984e4-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="984e4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="984e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="984e4-105">A documentação do SDK do Windows inclui uma discussão abrangente das regras para implementar objetos em conformidade com o COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="984e4-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="984e4-106">Essas regras abordam como fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="984e4-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="984e4-107">Projetar interfaces e objetos.</span><span class="sxs-lookup"><span data-stu-id="984e4-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="984e4-108">Implemente a interface [IUnknown.](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="984e4-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="984e4-109">Gerenciar memória.</span><span class="sxs-lookup"><span data-stu-id="984e4-109">Manage memory.</span></span>
    
- <span data-ttu-id="984e4-110">Lidar com a contagem de referências.</span><span class="sxs-lookup"><span data-stu-id="984e4-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="984e4-111">Implemente objetos apartment-threaded.</span><span class="sxs-lookup"><span data-stu-id="984e4-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="984e4-112">Embora todos os objetos MAPI sejam considerados baseados em COM porque implementam interfaces que herdam de [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI se desvia em algumas situações das regras COM padrão.</span><span class="sxs-lookup"><span data-stu-id="984e4-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="984e4-113">Esse desvio permite aos desenvolvedores mais flexibilidade em suas implementações.</span><span class="sxs-lookup"><span data-stu-id="984e4-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="984e4-114">Por exemplo, uma interface MAPI, como qualquer interface COM, descreve um contrato entre o implementador e o chamador.</span><span class="sxs-lookup"><span data-stu-id="984e4-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="984e4-115">Depois que a interface é criada e publicada, sua definição não pode e não muda.</span><span class="sxs-lookup"><span data-stu-id="984e4-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="984e4-116">O MAPI não se desvia dessa descrição, mas a descrição é um pouco diferente.</span><span class="sxs-lookup"><span data-stu-id="984e4-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="984e4-117">Implementadores podem optar por não implementar métodos específicos, retornando um dos seguintes valores de erro para o chamador:</span><span class="sxs-lookup"><span data-stu-id="984e4-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="984e4-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="984e4-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="984e4-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="984e4-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="984e4-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="984e4-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="984e4-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="984e4-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="984e4-122">Os outros desvios das regras COM padrão são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="984e4-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="984e4-123">**Regra de programação COM**</span><span class="sxs-lookup"><span data-stu-id="984e4-123">**COM programming rule**</span></span>|<span data-ttu-id="984e4-124">**Variação MAPI**</span><span class="sxs-lookup"><span data-stu-id="984e4-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="984e4-125">Todos os parâmetros de cadeia de caracteres nos métodos de interface devem ser Unicode.</span><span class="sxs-lookup"><span data-stu-id="984e4-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="984e4-126">As interfaces MAPI são definidas para permitir parâmetros de cadeia de caracteres Unicode ou ANSI.</span><span class="sxs-lookup"><span data-stu-id="984e4-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="984e4-127">Muitos métodos que têm um parâmetro de cadeia de caracteres também têm um **parâmetro ulFlags;** a largura de um parâmetro de cadeia de caracteres é indicada pelo valor do MAPI_UNICODE sinalizador em **ulFlags**.</span><span class="sxs-lookup"><span data-stu-id="984e4-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="984e4-128">Algumas interfaces MAPI não suportam Unicode e retornam MAPI_E_BAD_CHARWIDTH quando o sinalizador MAPI_UNICODE está definido.</span><span class="sxs-lookup"><span data-stu-id="984e4-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="984e4-129">Todos os métodos de interface devem ter um tipo de retorno HRESULT.</span><span class="sxs-lookup"><span data-stu-id="984e4-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="984e4-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="984e4-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="984e4-131">Os chamadores e implementadores devem alocar e liberar memória para parâmetros de interface usando os alocadores de tarefas COM padrão.</span><span class="sxs-lookup"><span data-stu-id="984e4-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="984e4-132">Todos os métodos MAPI usam os alocadores vinculados [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md) para gerenciar a memória para parâmetros de interface.</span><span class="sxs-lookup"><span data-stu-id="984e4-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="984e4-133">Todas as implementações de MAPI de interfaces definidas por OLE, como [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)usam os alocadores de tarefas COM padrão.</span><span class="sxs-lookup"><span data-stu-id="984e4-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="984e4-134">Todos os parâmetros de ponteiro de saída devem ser definidos explicitamente como NULL quando um método falhar.</span><span class="sxs-lookup"><span data-stu-id="984e4-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="984e4-135">As interfaces MAPI exigem que os parâmetros de ponteiro de saída sejam definidos como NULL ou permaneçam inalterados quando um método falha.</span><span class="sxs-lookup"><span data-stu-id="984e4-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="984e4-136">Todas as implementações de MAPI de interfaces definidas pelo OLE explicitamente definem parâmetros como NULL em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="984e4-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="984e4-137">Implemente objetos aggregatable sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="984e4-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="984e4-138">As interfaces MAPI não são aggregantes.</span><span class="sxs-lookup"><span data-stu-id="984e4-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="984e4-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="984e4-139">See also</span></span>



[<span data-ttu-id="984e4-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="984e4-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="984e4-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="984e4-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="984e4-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="984e4-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="984e4-143">Visão geral de objetos e interface MAPI</span><span class="sxs-lookup"><span data-stu-id="984e4-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

