---
title: Implementação do objeto Control
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8304021565638f8a5893d0be8cd6a94ed62a8d95
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422604"
---
# <a name="control-object-implementation"></a><span data-ttu-id="1e0b5-103">Implementação do objeto Control</span><span class="sxs-lookup"><span data-stu-id="1e0b5-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="1e0b5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e0b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e0b5-105">Objetos de controle, ou objetos que oferecem suporte à interface [IMAPIControl: IUnknown](imapicontroliunknown.md) , são implementados por provedores para adicionar funcionalidade a um botão que aparece em uma caixa de diálogo MAPI.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="1e0b5-106">Os objetos Control só podem ser implementados para botões.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="1e0b5-107">O **IMAPIControl** tem três métodos [](imapicontrol-getlasterror.md): GetLastError [](imapicontrol-getstate.md), GetState e [Activate](imapicontrol-activate.md).</span><span class="sxs-lookup"><span data-stu-id="1e0b5-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="1e0b5-108">MAPI chama **GetState** para determinar se o botão deve ou não ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="1e0b5-109">**GetState** é chamado nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="1e0b5-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="1e0b5-110">Quando a caixa de diálogo na qual o botão aparece é exibida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="1e0b5-111">Quando uma notificação de tabela de exibição é emitida para o botão.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="1e0b5-112">Defina o conteúdo do parâmetro _lpulState_ como MAPI_DISABLED se o usuário não puder interagir com o botão e MAPI_ENABLED se o usuário puder interagir.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="1e0b5-113">Quando o usuário clica no botão, as chamadas \*\*\*\* MAPI são ativadas.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="1e0b5-114">**Activate** executa a tarefa que foi associada ao botão.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="1e0b5-115">Essa tarefa pode ser algo apropriado para o seu provedor, como exibir uma caixa de diálogo ou atualizar uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="1e0b5-116">Se a tarefa não tiver êxito porque o usuário a cancelou, retorne MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="1e0b5-117">Para outras causas de falha, retorne o valor de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="1e0b5-118">Se a tarefa for bem-sucedida e estiver vinculada a uma alteração de propriedade que é refletida em outro controle na caixa de diálogo, chame [ITableData:: HrNotify](itabledata-hrnotify.md).</span><span class="sxs-lookup"><span data-stu-id="1e0b5-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="1e0b5-119">**HrNotify** é chamado para emitir uma notificação de exibição da tabela com a propriedade **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) da propriedade Changed na estrutura [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="1e0b5-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="1e0b5-120">Não coloque o novo valor da propriedade na estrutura; em vez disso, retorne-a quando [IMAPIProp::](imapiprop-getprops.md) GetProps for chamado.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="1e0b5-121">Embora normalmente uma notificação de tabela de exibição não possa ser usada para desabilitar ou habilitar um controle, ela pode ser usada com um botão.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="1e0b5-122">O MAPI atualizará o controle alterado para responder à notificação.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="1e0b5-123">MAPI chama o método **GetLastError** do controle quando **Activate** retorna um erro diferente de MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="1e0b5-124">Se **GetLastError** colocar informações de erro estendidas na estrutura [MAPIERROR](mapierror.md) que retorna no conteúdo do parâmetro _lppMAPIError_ , MAPI a exibe para o usuário.</span><span class="sxs-lookup"><span data-stu-id="1e0b5-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1e0b5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e0b5-125">See also</span></span>



[<span data-ttu-id="1e0b5-126">Provedores de serviço MAPI</span><span class="sxs-lookup"><span data-stu-id="1e0b5-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

