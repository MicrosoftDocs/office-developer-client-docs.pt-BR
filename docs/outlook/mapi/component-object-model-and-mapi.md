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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394115"
---
# <a name="component-object-model-and-mapi"></a><span data-ttu-id="c6083-103">COM (Component Object Model) e MAPI</span><span class="sxs-lookup"><span data-stu-id="c6083-103">Component Object Model and MAPI</span></span>

  
  
<span data-ttu-id="c6083-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6083-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6083-105">Documentação do SDK do Windows inclui uma discussão abrangente das regras de implementação de objetos que se ajustam para o modelo COM (Component Object).</span><span class="sxs-lookup"><span data-stu-id="c6083-105">The Windows SDK documentation includes a comprehensive discussion of the rules for implementing objects that conform to the Component Object Model (COM).</span></span> <span data-ttu-id="c6083-106">Essas regras tratam como fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c6083-106">These rules address how to do the following:</span></span>
  
- <span data-ttu-id="c6083-107">Objetos e interfaces de design.</span><span class="sxs-lookup"><span data-stu-id="c6083-107">Design interfaces and objects.</span></span>
    
- <span data-ttu-id="c6083-108">Implemente a interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c6083-108">Implement the [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) interface.</span></span> 
    
- <span data-ttu-id="c6083-109">Gerencie memória.</span><span class="sxs-lookup"><span data-stu-id="c6083-109">Manage memory.</span></span>
    
- <span data-ttu-id="c6083-110">Lidar com a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="c6083-110">Handle reference counting.</span></span>
    
- <span data-ttu-id="c6083-111">Implemente objetos de apartamento.</span><span class="sxs-lookup"><span data-stu-id="c6083-111">Implement apartment-threaded objects.</span></span>
    
<span data-ttu-id="c6083-112">Embora todos os objetos MAPI são considerados baseado em COM, porque eles implementam as interfaces que herdam [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI difere em determinadas situações de regras COM standard.</span><span class="sxs-lookup"><span data-stu-id="c6083-112">Although all MAPI objects are considered COM-based because they implement interfaces that inherit from [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx), MAPI deviates in some situations from the standard COM rules.</span></span> <span data-ttu-id="c6083-113">Este desvio permite aos desenvolvedores mais flexibilidade em suas implementações.</span><span class="sxs-lookup"><span data-stu-id="c6083-113">This deviation allows developers more flexibility in their implementations.</span></span> <span data-ttu-id="c6083-114">Por exemplo, uma interface MAPI, como qualquer interface COM, descreve um contrato entre o chamador e o implementador.</span><span class="sxs-lookup"><span data-stu-id="c6083-114">For example, a MAPI interface, like any COM interface, describes a contract between implementer and caller.</span></span> <span data-ttu-id="c6083-115">Depois que a interface é criada e publicada, sua definição não é possível e não é alterado.</span><span class="sxs-lookup"><span data-stu-id="c6083-115">Once the interface is created and published, its definition cannot and does not change.</span></span> <span data-ttu-id="c6083-116">MAPI não desviar dessa descrição, mas ele libera a descrição relativamente.</span><span class="sxs-lookup"><span data-stu-id="c6083-116">MAPI does not deviate from this description, but it relaxes the description somewhat.</span></span> <span data-ttu-id="c6083-117">Implementadores podem optar por não implementar os métodos específicos, o retorno de um dos seguintes valores de erro ao chamador:</span><span class="sxs-lookup"><span data-stu-id="c6083-117">Implementers can choose to not implement particular methods, returning one of the following error values to the caller:</span></span> 
  
- <span data-ttu-id="c6083-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c6083-118">MAPI_E_NO_SUPPORT</span></span>
    
- <span data-ttu-id="c6083-119">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="c6083-119">MAPI_E_TOO_COMPLEX</span></span>
    
- <span data-ttu-id="c6083-120">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c6083-120">MAPI_E_BAD_CHARWIDTH</span></span>
    
- <span data-ttu-id="c6083-121">MAPI_E_TYPE_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="c6083-121">MAPI_E_TYPE_NO_SUPPORT</span></span>
    
<span data-ttu-id="c6083-122">Os outros desvios das regras COM standard são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c6083-122">The other deviations from the standard COM rules are described in the following table.</span></span>
  
|<span data-ttu-id="c6083-123">**Regra de programação COM**</span><span class="sxs-lookup"><span data-stu-id="c6083-123">**COM programming rule**</span></span>|<span data-ttu-id="c6083-124">**Variação de MAPI**</span><span class="sxs-lookup"><span data-stu-id="c6083-124">**MAPI variation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6083-125">Todos os parâmetros de cadeia de caracteres nos métodos de interface devem ser Unicode.</span><span class="sxs-lookup"><span data-stu-id="c6083-125">All string parameters in interface methods should be Unicode.</span></span>  <br/> |<span data-ttu-id="c6083-126">Interfaces MAPI são definidas para permitir que os parâmetros de cadeia de caracteres Unicode ou ANSI.</span><span class="sxs-lookup"><span data-stu-id="c6083-126">MAPI interfaces are defined to permit either Unicode or ANSI string parameters.</span></span> <span data-ttu-id="c6083-127">Muitos métodos que têm um parâmetro de cadeia de caracteres também tem um parâmetro de **ulFlags** ; a largura de um parâmetro de cadeia de caracteres é indicada pelo valor do sinalizador MAPI_UNICODE em **ulFlags**.</span><span class="sxs-lookup"><span data-stu-id="c6083-127">Many methods that have a string parameter also have a **ulFlags** parameter; the width of a string parameter is indicated by the value of the MAPI_UNICODE flag in **ulFlags**.</span></span> <span data-ttu-id="c6083-128">Algumas interfaces MAPI não oferece suporte a Unicode e retornar MAPI_E_BAD_CHARWIDTH quando o sinalizador MAPI_UNICODE é definido.</span><span class="sxs-lookup"><span data-stu-id="c6083-128">Some MAPI interfaces do not support Unicode and return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is set.</span></span>  <br/> |
|<span data-ttu-id="c6083-129">Todos os métodos de interface devem ter um tipo de retorno de HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c6083-129">All interface methods should have a return type of HRESULT.</span></span>  <br/> |<span data-ttu-id="c6083-130">MAPI tem pelo menos um método que retorna um valor não-HRESULT: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="c6083-130">MAPI has at least one method that returns a non-HRESULT value: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).</span></span>  <br/> |
|<span data-ttu-id="c6083-131">Os chamadores e implementadores devem alocar e liberar memória para os parâmetros de interface usando os alocadores de tarefa COM standard.</span><span class="sxs-lookup"><span data-stu-id="c6083-131">Callers and implementers should allocate and free memory for interface parameters by using the standard COM task allocators.</span></span>  <br/> |<span data-ttu-id="c6083-132">Todos os métodos MAPI usam os vinculados alocadores [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md) para gerenciar memória para os parâmetros de interface.</span><span class="sxs-lookup"><span data-stu-id="c6083-132">All MAPI methods use the linked allocators [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) to manage memory for interface parameters.</span></span> <span data-ttu-id="c6083-133">Todas as implementações de MAPI das interfaces definidos pelo OLE, como [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), usam os alocadores de tarefa COM standard.</span><span class="sxs-lookup"><span data-stu-id="c6083-133">All MAPI implementations of interfaces defined by OLE, such as [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx), use the standard COM task allocators.</span></span>  <br/> |
|<span data-ttu-id="c6083-134">A saída todos os parâmetros de ponteiro explicitamente devem ser definidos como NULL quando um método falha.</span><span class="sxs-lookup"><span data-stu-id="c6083-134">All out pointer parameters must explicitly be set to NULL when a method fails.</span></span>  <br/> |<span data-ttu-id="c6083-135">Interfaces de MAPI exigem que os parâmetros de ponteiro estar definido como NULL ou permanecer inalterado quando um método de saída falhar.</span><span class="sxs-lookup"><span data-stu-id="c6083-135">MAPI interfaces require that out pointer parameters either be set to NULL or remain unchanged when a method fails.</span></span> <span data-ttu-id="c6083-136">Todas as implementações de MAPI das interfaces definidos pelo OLE explicitamente definir parâmetros como NULL em caso de falha de saída.</span><span class="sxs-lookup"><span data-stu-id="c6083-136">All MAPI implementations of interfaces defined by OLE explicitly set out parameters to NULL on failure.</span></span>  <br/> |
|<span data-ttu-id="c6083-137">Implemente objetos de endereços sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="c6083-137">Implement aggregatable objects whenever possible.</span></span>  <br/> |<span data-ttu-id="c6083-138">Interfaces MAPI não são agregáveis.</span><span class="sxs-lookup"><span data-stu-id="c6083-138">MAPI interfaces are not aggregatable.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6083-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6083-139">See also</span></span>



[<span data-ttu-id="c6083-140">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c6083-140">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="c6083-141">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="c6083-141">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="c6083-142">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c6083-142">MAPIFreeBuffer</span></span>](mapifreebuffer.md)


[<span data-ttu-id="c6083-143">Objeto MAPI e visão geral da Interface</span><span class="sxs-lookup"><span data-stu-id="c6083-143">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

