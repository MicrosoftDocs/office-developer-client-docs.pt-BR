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
ms.openlocfilehash: 8dce1415ef8d18f4b786e92324c888f9a0845162
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414036"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="e8b1e-103">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e8b1e-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="e8b1e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8b1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8b1e-105">Habilita e desabilita um controle de botão e realiza tarefas quando um usuário de um aplicativo cliente clica no controle habilitado.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="e8b1e-106">Os provedores de serviços implementam objetos de controle para criar botões personalizados em caixas de diálogo, como as folhas de propriedades de configuração, que são definidas usando as tabelas de exibição.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="e8b1e-107">Para obter mais informações sobre como trabalhar com tabelas de exibição e objetos de controle, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e8b1e-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8b1e-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e8b1e-108">Header file:</span></span>  <br/> |<span data-ttu-id="e8b1e-109">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e8b1e-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e8b1e-110">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="e8b1e-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="e8b1e-111">Objetos de controle</span><span class="sxs-lookup"><span data-stu-id="e8b1e-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="e8b1e-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e8b1e-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="e8b1e-113">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="e8b1e-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="e8b1e-114">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="e8b1e-114">Called by:</span></span>  <br/> |<span data-ttu-id="e8b1e-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="e8b1e-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="e8b1e-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="e8b1e-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e8b1e-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="e8b1e-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="e8b1e-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="e8b1e-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="e8b1e-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="e8b1e-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e8b1e-120">Vtable order</span><span class="sxs-lookup"><span data-stu-id="e8b1e-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e8b1e-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="e8b1e-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="e8b1e-122">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de controle de botão anterior.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="e8b1e-123">Activate</span><span class="sxs-lookup"><span data-stu-id="e8b1e-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="e8b1e-124">Executa uma tarefa, como exibir uma caixa de diálogo ou iniciar uma operação programática quando um usuário de aplicativo cliente clica no controle de botão.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="e8b1e-125">GetState</span><span class="sxs-lookup"><span data-stu-id="e8b1e-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="e8b1e-126">Recupera um valor que indica se o controle de botão está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e8b1e-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8b1e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8b1e-127">See also</span></span>



[<span data-ttu-id="e8b1e-128">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e8b1e-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

