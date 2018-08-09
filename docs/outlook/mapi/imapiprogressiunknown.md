---
title: IMAPIProgress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 975c01457515a400d1d442fedc432dc000f06665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767143"
---
# <a name="imapiprogress--iunknown"></a><span data-ttu-id="41269-103">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="41269-103">IMAPIProgress : IUnknown</span></span>

  
  
<span data-ttu-id="41269-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41269-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="41269-105">Implementa um objeto de progresso que fornece aos aplicativos de cliente com um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="41269-105">Implements a progress object that provides client applications with a progress indicator.</span></span> <span data-ttu-id="41269-106">Um indicador de progresso é uma exibição da interface do usuário que mostra a porcentagem de conclusão de uma operação, como copiar pastas entre as lojas de mensagem.</span><span class="sxs-lookup"><span data-stu-id="41269-106">A progress indicator is a user-interface display that shows the percentage of completion of an operation, such as copying folders between message stores.</span></span> <span data-ttu-id="41269-107">Aplicativos MAPI e cliente implementam objetos de progresso e provedores de serviços de usá-los.</span><span class="sxs-lookup"><span data-stu-id="41269-107">MAPI and client applications implement progress objects and service providers use them.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41269-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="41269-108">Header file:</span></span>  <br/> |<span data-ttu-id="41269-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41269-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="41269-110">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="41269-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="41269-111">Objetos de progresso</span><span class="sxs-lookup"><span data-stu-id="41269-111">Progress objects</span></span>  <br/> |
|<span data-ttu-id="41269-112">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="41269-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="41269-113">Aplicativos MAPI e cliente</span><span class="sxs-lookup"><span data-stu-id="41269-113">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="41269-114">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="41269-114">Called by:</span></span>  <br/> |<span data-ttu-id="41269-115">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="41269-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="41269-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="41269-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="41269-117">IID_IMAPIProgress</span><span class="sxs-lookup"><span data-stu-id="41269-117">IID_IMAPIProgress</span></span>  <br/> |
|<span data-ttu-id="41269-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="41269-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="41269-119">LPMAPIPROGRESS</span><span class="sxs-lookup"><span data-stu-id="41269-119">LPMAPIPROGRESS</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="41269-120">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="41269-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="41269-121">Progress</span><span class="sxs-lookup"><span data-stu-id="41269-121">Progress</span></span>](imapiprogress-progress.md) <br/> |<span data-ttu-id="41269-122">Atualiza o indicador de progresso com uma exibição do progresso da conforme ele é feito rumo à conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="41269-122">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span>  <br/> |
|[<span data-ttu-id="41269-123">GetFlags</span><span class="sxs-lookup"><span data-stu-id="41269-123">GetFlags</span></span>](imapiprogress-getflags.md) <br/> |<span data-ttu-id="41269-124">Retorna sinaliza as configurações do objeto de andamento para o nível de operação no qual as informações sobre o andamento é calculado.</span><span class="sxs-lookup"><span data-stu-id="41269-124">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>  <br/> |
|[<span data-ttu-id="41269-125">GetMax</span><span class="sxs-lookup"><span data-stu-id="41269-125">GetMax</span></span>](imapiprogress-getmax.md) <br/> |<span data-ttu-id="41269-126">Retorna o número máximo de itens na operação para o qual andamento informações são exibidas.</span><span class="sxs-lookup"><span data-stu-id="41269-126">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="41269-127">GetMin</span><span class="sxs-lookup"><span data-stu-id="41269-127">GetMin</span></span>](imapiprogress-getmin.md) <br/> |<span data-ttu-id="41269-128">Retorna o valor mínimo no método [SetLimits](imapiprogress-setlimits.md) para qual andamento informações são exibidas.</span><span class="sxs-lookup"><span data-stu-id="41269-128">Returns the minimum value in the [SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="41269-129">SetLimits</span><span class="sxs-lookup"><span data-stu-id="41269-129">SetLimits</span></span>](imapiprogress-setlimits.md) <br/> |<span data-ttu-id="41269-130">Define os limites inferiores e superiores para o número de itens da operação e os sinalizadores que controlam como as informações sobre o andamento é calculada para a operação.</span><span class="sxs-lookup"><span data-stu-id="41269-130">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41269-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="41269-131">Remarks</span></span>

<span data-ttu-id="41269-132">MAPI inclui um parâmetro _lpProgress_ em muitos dos métodos que executam operações potencialmente demoradas.</span><span class="sxs-lookup"><span data-stu-id="41269-132">MAPI includes an  _lpProgress_ parameter in many of the methods that perform potentially lengthy operations.</span></span>  <span data-ttu-id="41269-133">_lpProgress_ aponta para uma implementação do cliente de um objeto de andamento.</span><span class="sxs-lookup"><span data-stu-id="41269-133">_lpProgress_ points to a client implementation of a progress object.</span></span> <span data-ttu-id="41269-134">Clientes que implementam a interface **IMAPIProgress** defina esse parâmetro para apontar para sua implementação; clientes que não implementam **IMAPIProgress** defina o parâmetro como NULL.</span><span class="sxs-lookup"><span data-stu-id="41269-134">Clients that implement the **IMAPIProgress** interface set this parameter to point to their implementation; clients that do not implement **IMAPIProgress** set the parameter to NULL.</span></span> <span data-ttu-id="41269-135">Para exibir um indicador de progresso durante o processamento da operação, provedores de serviços usam o objeto de progresso fornecido pelo cliente, se disponível, ou uma implementação de MAPI (indicada quando _lpProgress_ estiver definido como NULL).</span><span class="sxs-lookup"><span data-stu-id="41269-135">To display a progress indicator during processing of the operation, service providers use the progress object supplied by the client, if available, or a MAPI implementation (indicated when  _lpProgress_ is set to NULL).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="41269-136">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="41269-136">MFCMAPI reference</span></span>

<span data-ttu-id="41269-137">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="41269-137">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="41269-138">**Arquivos**</span><span class="sxs-lookup"><span data-stu-id="41269-138">**Files**</span></span>|<span data-ttu-id="41269-139">**Function**</span><span class="sxs-lookup"><span data-stu-id="41269-139">**Function**</span></span>|<span data-ttu-id="41269-140">**Comment**</span><span class="sxs-lookup"><span data-stu-id="41269-140">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="41269-141">MapiProgress.h e MapiProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="41269-141">MapiProgress.h and MapiProgress.cpp</span></span>  <br/> |<span data-ttu-id="41269-142">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="41269-142">Not applicable</span></span>  <br/> |<span data-ttu-id="41269-143">Se a configuração IMAPIProgress estiver habilitada, MFCMAPI passará uma implementação **IMAPIProgress** a todas as funções que invoca MFCMAPI que aceitam uma implementação.</span><span class="sxs-lookup"><span data-stu-id="41269-143">If the IMAPIProgress setting is enabled, MFCMAPI will pass an **IMAPIProgress** implementation to all functions that MFCMAPI invokes that accept an implementation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41269-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="41269-144">See also</span></span>



[<span data-ttu-id="41269-145">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="41269-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="41269-146">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="41269-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

