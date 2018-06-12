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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 395e44c2ea54816fab9f29dbedfe5e165e98c7b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766945"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="12534-103">IMAPIControl: IUnknown</span><span class="sxs-lookup"><span data-stu-id="12534-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="12534-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="12534-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="12534-105">Habilita e desabilita a um controle de botão e executa tarefas quando um usuário de um aplicativo cliente clica no controle habilitado.</span><span class="sxs-lookup"><span data-stu-id="12534-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="12534-106">Provedores de serviço implementar objetos de controle para criar botões personalizados em caixas de diálogo, como folhas de propriedades de configuração, que são definidas por meio de tabelas de exibição.</span><span class="sxs-lookup"><span data-stu-id="12534-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="12534-107">Para obter mais informações sobre como trabalhar com tabelas de exibição e controlar objetos, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="12534-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12534-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="12534-108">Header file:</span></span>  <br/> |<span data-ttu-id="12534-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12534-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="12534-110">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="12534-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="12534-111">Objetos de controle</span><span class="sxs-lookup"><span data-stu-id="12534-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="12534-112">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="12534-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="12534-113">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="12534-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="12534-114">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="12534-114">Called by:</span></span>  <br/> |<span data-ttu-id="12534-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="12534-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="12534-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="12534-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="12534-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="12534-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="12534-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="12534-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="12534-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="12534-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="12534-120">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="12534-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="12534-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="12534-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="12534-122">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de controle de botão anterior.</span><span class="sxs-lookup"><span data-stu-id="12534-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="12534-123">Ativar</span><span class="sxs-lookup"><span data-stu-id="12534-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="12534-124">Executa uma tarefa como exibir uma caixa de diálogo ou iniciar uma operação programática quando um usuário do aplicativo cliente clica no controle de botão.</span><span class="sxs-lookup"><span data-stu-id="12534-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="12534-125">GetState</span><span class="sxs-lookup"><span data-stu-id="12534-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="12534-126">Recupera um valor que indica se o controle de botão está ativado ou desativado.</span><span class="sxs-lookup"><span data-stu-id="12534-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="12534-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="12534-127">See also</span></span>



[<span data-ttu-id="12534-128">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="12534-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

