---
title: Implementação de objeto do controle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 268ad60cf8161fb2b58370f89aae623aabd7da7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766318"
---
# <a name="control-object-implementation"></a><span data-ttu-id="5cbff-103">Implementação de objeto do controle</span><span class="sxs-lookup"><span data-stu-id="5cbff-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="5cbff-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5cbff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5cbff-105">Controlar objetos ou objetos que suportam o [IMAPIControl: IUnknown](imapicontroliunknown.md) interface, são implementadas pelos provedores para adicionar funcionalidades a um botão que aparece em uma caixa de diálogo MAPI.</span><span class="sxs-lookup"><span data-stu-id="5cbff-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="5cbff-106">Objetos de controle só podem ser implementados para botões.</span><span class="sxs-lookup"><span data-stu-id="5cbff-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="5cbff-107">**IMAPIControl** possui três métodos: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md)e [Ativar](imapicontrol-activate.md).</span><span class="sxs-lookup"><span data-stu-id="5cbff-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="5cbff-108">**GetState** para determinar se ou não desabilitar o botão de chamadas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="5cbff-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="5cbff-109">**GetState** é chamado nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="5cbff-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="5cbff-110">Quando a caixa de diálogo na qual o botão aparece primeiro é exibida.</span><span class="sxs-lookup"><span data-stu-id="5cbff-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="5cbff-111">Quando uma notificação de tabela de exibição é emitida para o botão.</span><span class="sxs-lookup"><span data-stu-id="5cbff-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="5cbff-112">Defina o conteúdo do parâmetro _lpulState_ para MAPI_DISABLED se o usuário não pode interagir com o botão e MAPI_ENABLED se o usuário pode interagir.</span><span class="sxs-lookup"><span data-stu-id="5cbff-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="5cbff-113">Quando o usuário clica no botão, **Ativar**chamadas MAPI.</span><span class="sxs-lookup"><span data-stu-id="5cbff-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="5cbff-114">**Ativar** realiza a tarefa que tenha sido associada ao botão.</span><span class="sxs-lookup"><span data-stu-id="5cbff-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="5cbff-115">Essa tarefa pode ser qualquer coisa apropriado para seu provedor, como exibir uma caixa de diálogo ou atualizar uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="5cbff-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="5cbff-116">Se a tarefa for bem sucedida porque o usuário cancelou a ele, retorne MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="5cbff-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="5cbff-117">Para outras causas de falha, retorne o valor de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="5cbff-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="5cbff-118">Se a tarefa for bem-sucedida e for vinculado a uma alteração de propriedade refletidos em outro controle, na caixa de diálogo, chame [ITableData::HrNotify](itabledata-hrnotify.md).</span><span class="sxs-lookup"><span data-stu-id="5cbff-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="5cbff-119">**HrNotify** é chamado para emitir uma notificação de tabela de exibição com a propriedade de **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) da propriedade alterados na estrutura [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="5cbff-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="5cbff-120">Não coloque o novo valor da propriedade na estrutura; em vez disso, retorná-lo quando [IMAPIProp::GetProps](imapiprop-getprops.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="5cbff-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="5cbff-121">Embora normalmente uma notificação de tabela de exibição não pode ser usada para desabilitar ou habilitar um controle, ele pode ser usado com um botão.</span><span class="sxs-lookup"><span data-stu-id="5cbff-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="5cbff-122">MAPI atualizará o controle alterado para responder à notificação.</span><span class="sxs-lookup"><span data-stu-id="5cbff-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="5cbff-123">MAPI chama o método do controle **GetLastError** quando **Ativar** retornará um erro que não seja MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="5cbff-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="5cbff-124">Se **GetLastError** colocará informações de erro estendidas na estrutura [MAPIERROR](mapierror.md) que ele retorna o conteúdo do parâmetro _lppMAPIError_ , MAPI exibe para o usuário.</span><span class="sxs-lookup"><span data-stu-id="5cbff-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5cbff-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cbff-125">See also</span></span>



[<span data-ttu-id="5cbff-126">Provedores de serviços MAPI</span><span class="sxs-lookup"><span data-stu-id="5cbff-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

