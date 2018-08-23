---
title: Exibindo informações do destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4610d9e643541e39144f2af86a2d64928b8e9ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591286"
---
# <a name="displaying-recipient-information"></a><span data-ttu-id="2a628-103">Exibindo informações do destinatário</span><span class="sxs-lookup"><span data-stu-id="2a628-103">Displaying recipient information</span></span>

<span data-ttu-id="2a628-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a628-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a628-105">MAPI fornece uma caixa de diálogo comuns para mostrar detalhes do destinatário.</span><span class="sxs-lookup"><span data-stu-id="2a628-105">MAPI provides a common dialog box for showing recipient details.</span></span> <span data-ttu-id="2a628-106">A caixa de diálogo detalhes é criada a partir de uma tabela de exibição e uma implementação **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="2a628-106">The details dialog box is created from a display table and an **IMAPIProp** implementation.</span></span> <span data-ttu-id="2a628-107">A tabela de exibição descreve a aparência da exibição detalhes e a implementação de **IMAPIProp** controla os dados para o destinatário.</span><span class="sxs-lookup"><span data-stu-id="2a628-107">The display table describes the appearance of the details display and the **IMAPIProp** implementation controls the data for the recipient.</span></span> <span data-ttu-id="2a628-108">Seu provedor é responsável por fornecer a tabela de exibição e a implementação de **IMAPIProp** para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="2a628-108">Your provider is responsible for supplying the display table and the **IMAPIProp** implementation for each recipient.</span></span> 
  
<span data-ttu-id="2a628-109">A maneira mais fácil para criar a tabela de exibição é definir uma estrutura [DTPAGE](dtpage.md) e [BuildDisplayTable](builddisplaytable.md)de chamada.</span><span class="sxs-lookup"><span data-stu-id="2a628-109">The easiest way to create the display table is to define a [DTPAGE](dtpage.md) structure and call [BuildDisplayTable](builddisplaytable.md).</span></span> <span data-ttu-id="2a628-110">No entanto, alguns provedores, especificamente provedores somente leitura que permitem a criação de destinatários únicos, usam **IPropData**.</span><span class="sxs-lookup"><span data-stu-id="2a628-110">However, some providers, specifically read-only providers that allow the creation of one-off recipients, use **IPropData**.</span></span> <span data-ttu-id="2a628-111">A implementação de **IMAPIProp** pode ser qualquer tipo de objeto de propriedade.</span><span class="sxs-lookup"><span data-stu-id="2a628-111">The **IMAPIProp** implementation can be any type of property object.</span></span> 
  
<span data-ttu-id="2a628-112">Há dois métodos para esta caixa de diálogo de invocação: [IAddrBook::Details](iaddrbook-details.md) e [IMAPISupport::Details](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="2a628-112">There are two methods for invoking this dialog box: [IAddrBook::Details](iaddrbook-details.md) and [IMAPISupport::Details](imapisupport-details.md).</span></span> <span data-ttu-id="2a628-113">Quando seu provedor chama um destes métodos para solicitar detalhes para um destinatário, MAPI primeiro abre o destinatário chamando o método de [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) do seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="2a628-113">When your provider calls one of these methods to request details for a recipient, MAPI first opens the recipient by calling its container's [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method.</span></span> <span data-ttu-id="2a628-114">Em seguida, ele chama o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do destinatário para solicitar a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2a628-114">Next it calls the recipient's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to request the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="2a628-115">**PR_DETAILS_TABLE** é a propriedade que representa a tabela de exibição de detalhes de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="2a628-115">**PR_DETAILS_TABLE** is the property that represents a recipient's details display table.</span></span> 
  
<span data-ttu-id="2a628-116">O [IPropData: IMAPIProp](ipropdataimapiprop.md) interface pode ser usado para monitorar alterações nos controles de exibição de tabela, conforme descrito no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="2a628-116">The [IPropData : IMAPIProp](ipropdataimapiprop.md) interface can be used to monitor changes on display table controls as described in the following procedure.</span></span> 
  
## <a name="monitor-changes-to-a-control"></a><span data-ttu-id="2a628-117">Monitore as alterações em um controle</span><span class="sxs-lookup"><span data-stu-id="2a628-117">Monitor changes to a control</span></span>
  
1. <span data-ttu-id="2a628-118">Antes do usuário obtiver acesso ao controle, chame [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) para definir o acesso do controle como IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="2a628-118">Before the user gains access to the control, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) to set the control's access to IPROP_CLEAN.</span></span> 
    
2. <span data-ttu-id="2a628-119">Permitir que o usuário trabalhar com a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2a628-119">Allow the user to work with the dialog box.</span></span> 
    
3. <span data-ttu-id="2a628-120">Quando o usuário tiver terminado, chame [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) para recuperar o nível de acesso atual do controle.</span><span class="sxs-lookup"><span data-stu-id="2a628-120">When the user has finished, call [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) to retrieve the current access level of the control.</span></span> 
    
4. <span data-ttu-id="2a628-121">Se o nível de acesso for IPROP_DIRTY, o usuário tiver modificado o controle.</span><span class="sxs-lookup"><span data-stu-id="2a628-121">If the access level is IPROP_DIRTY, the user has modified the control.</span></span> <span data-ttu-id="2a628-122">Seu provedor deve:</span><span class="sxs-lookup"><span data-stu-id="2a628-122">Your provider should:</span></span>
    
   - <span data-ttu-id="2a628-123">Chame [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) para definir o acesso do nível de volta ao IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="2a628-123">Call [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) to set the access level back to IPROP_CLEAN.</span></span> 
    
   - <span data-ttu-id="2a628-124">Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do objeto de dados de propriedade para recuperar a propriedade alterada e atualizá-lo chamando [IMAPIProp::SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="2a628-124">Call the property data object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the changed property and update it by calling [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
5. <span data-ttu-id="2a628-125">Se o nível de acesso ainda IPROP_CLEAN, o controle não foi modificado.</span><span class="sxs-lookup"><span data-stu-id="2a628-125">If the access level is still IPROP_CLEAN, the control has not been modified.</span></span> 
    
<span data-ttu-id="2a628-126">Para obter mais informações sobre a criação de tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="2a628-126">For more information about creating display tables, see [Display Tables](display-tables.md).</span></span>
  

