---
title: IMAPIControl IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 80acb1a1e4663a68efc4692ab67ec27bc369f4b0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566513"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="4aab7-103">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4aab7-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="4aab7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4aab7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4aab7-105">Habilita e desabilita a um controle de botão e executa tarefas quando um usuário de um aplicativo cliente clica no controle habilitado.</span><span class="sxs-lookup"><span data-stu-id="4aab7-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="4aab7-106">Provedores de serviço implementar objetos de controle para criar botões personalizados em caixas de diálogo, como folhas de propriedades de configuração, que são definidas por meio de tabelas de exibição.</span><span class="sxs-lookup"><span data-stu-id="4aab7-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="4aab7-107">Para obter mais informações sobre como trabalhar com tabelas de exibição e controlar objetos, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4aab7-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4aab7-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4aab7-108">Header file:</span></span>  <br/> |<span data-ttu-id="4aab7-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4aab7-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4aab7-110">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="4aab7-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="4aab7-111">Objetos de controle</span><span class="sxs-lookup"><span data-stu-id="4aab7-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="4aab7-112">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="4aab7-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="4aab7-113">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="4aab7-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="4aab7-114">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="4aab7-114">Called by:</span></span>  <br/> |<span data-ttu-id="4aab7-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="4aab7-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="4aab7-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="4aab7-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4aab7-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="4aab7-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="4aab7-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="4aab7-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="4aab7-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="4aab7-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4aab7-120">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="4aab7-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4aab7-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="4aab7-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="4aab7-122">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de controle de botão anterior.</span><span class="sxs-lookup"><span data-stu-id="4aab7-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="4aab7-123">Ativar</span><span class="sxs-lookup"><span data-stu-id="4aab7-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="4aab7-124">Executa uma tarefa como exibir uma caixa de diálogo ou iniciar uma operação programática quando um usuário do aplicativo cliente clica no controle de botão.</span><span class="sxs-lookup"><span data-stu-id="4aab7-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="4aab7-125">GetState</span><span class="sxs-lookup"><span data-stu-id="4aab7-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="4aab7-126">Recupera um valor que indica se o controle de botão está ativado ou desativado.</span><span class="sxs-lookup"><span data-stu-id="4aab7-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4aab7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4aab7-127">See also</span></span>



[<span data-ttu-id="4aab7-128">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="4aab7-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

