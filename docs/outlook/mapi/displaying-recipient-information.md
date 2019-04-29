---
title: Exibir informações do destinatário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e1c31e5edf702dd8f172f67e7055a96ae4cfff1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412951"
---
# <a name="displaying-recipient-information"></a><span data-ttu-id="e0868-103">Exibir informações do destinatário</span><span class="sxs-lookup"><span data-stu-id="e0868-103">Displaying recipient information</span></span>

<span data-ttu-id="e0868-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0868-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0868-105">MAPI fornece uma caixa de diálogo comum para a exibição de detalhes do destinatário.</span><span class="sxs-lookup"><span data-stu-id="e0868-105">MAPI provides a common dialog box for showing recipient details.</span></span> <span data-ttu-id="e0868-106">A caixa de diálogo detalhes é criada a partir de uma tabela de exibição e de uma implementação do **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="e0868-106">The details dialog box is created from a display table and an **IMAPIProp** implementation.</span></span> <span data-ttu-id="e0868-107">A tabela de exibição descreve a aparência da exibição de detalhes e a implementação do **IMAPIProp** controla os dados do destinatário.</span><span class="sxs-lookup"><span data-stu-id="e0868-107">The display table describes the appearance of the details display and the **IMAPIProp** implementation controls the data for the recipient.</span></span> <span data-ttu-id="e0868-108">Seu provedor é responsável por fornecer a tabela de exibição e a implementação de **IMAPIProp** para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="e0868-108">Your provider is responsible for supplying the display table and the **IMAPIProp** implementation for each recipient.</span></span> 
  
<span data-ttu-id="e0868-109">A maneira mais fácil de criar a tabela de exibição é definir uma estrutura [DTPAGE](dtpage.md) e chamar [BuildDisplayTable](builddisplaytable.md).</span><span class="sxs-lookup"><span data-stu-id="e0868-109">The easiest way to create the display table is to define a [DTPAGE](dtpage.md) structure and call [BuildDisplayTable](builddisplaytable.md).</span></span> <span data-ttu-id="e0868-110">No enTanto, alguns provedores, especificamente provedores somente leitura que permitem a criação de destinatários únicos, usam **IPropData**.</span><span class="sxs-lookup"><span data-stu-id="e0868-110">However, some providers, specifically read-only providers that allow the creation of one-off recipients, use **IPropData**.</span></span> <span data-ttu-id="e0868-111">A implementação **IMAPIProp** pode ser qualquer tipo de objeto Property.</span><span class="sxs-lookup"><span data-stu-id="e0868-111">The **IMAPIProp** implementation can be any type of property object.</span></span> 
  
<span data-ttu-id="e0868-112">Há dois métodos para invocar esta caixa de diálogo: [IAddrBook::D etails](iaddrbook-details.md) e [IMAPISupport::D etails](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="e0868-112">There are two methods for invoking this dialog box: [IAddrBook::Details](iaddrbook-details.md) and [IMAPISupport::Details](imapisupport-details.md).</span></span> <span data-ttu-id="e0868-113">Quando o provedor chama um destes métodos para solicitar detalhes de um destinatário, o MAPI primeiro abre o destinatário chamando o método [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e0868-113">When your provider calls one of these methods to request details for a recipient, MAPI first opens the recipient by calling its container's [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method.</span></span> <span data-ttu-id="e0868-114">Em seguida, ele chama o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do destinatário para solicitar a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e0868-114">Next it calls the recipient's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to request the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="e0868-115">**PR_DETAILS_TABLE** é a propriedade que representa a tabela de exibição de detalhes de um destinatário.</span><span class="sxs-lookup"><span data-stu-id="e0868-115">**PR_DETAILS_TABLE** is the property that represents a recipient's details display table.</span></span> 
  
<span data-ttu-id="e0868-116">A interface [IPropData: IMAPIProp](ipropdataimapiprop.md) pode ser usada para monitorar as alterações nos controles da tabela de exibição, conforme descrito no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0868-116">The [IPropData : IMAPIProp](ipropdataimapiprop.md) interface can be used to monitor changes on display table controls as described in the following procedure.</span></span> 
  
## <a name="monitor-changes-to-a-control"></a><span data-ttu-id="e0868-117">Monitorar alterações em um controle</span><span class="sxs-lookup"><span data-stu-id="e0868-117">Monitor changes to a control</span></span>
  
1. <span data-ttu-id="e0868-118">Antes que o usuário tenha acesso ao controle, chame [IPropData:: HrSetObjAccess](ipropdata-hrsetobjaccess.md) para definir o acesso do controle ao IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="e0868-118">Before the user gains access to the control, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) to set the control's access to IPROP_CLEAN.</span></span> 
    
2. <span data-ttu-id="e0868-119">Permite que o usuário trabalhe com a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e0868-119">Allow the user to work with the dialog box.</span></span> 
    
3. <span data-ttu-id="e0868-120">Quando o usuário tiver concluído, chame [IPropData:: HrGetPropAccess](ipropdata-hrgetpropaccess.md) para recuperar o nível de acesso atual do controle.</span><span class="sxs-lookup"><span data-stu-id="e0868-120">When the user has finished, call [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) to retrieve the current access level of the control.</span></span> 
    
4. <span data-ttu-id="e0868-121">Se o nível de acesso for IPROP_DIRTY, o usuário modificou o controle.</span><span class="sxs-lookup"><span data-stu-id="e0868-121">If the access level is IPROP_DIRTY, the user has modified the control.</span></span> <span data-ttu-id="e0868-122">Seu provedor deve:</span><span class="sxs-lookup"><span data-stu-id="e0868-122">Your provider should:</span></span>
    
   - <span data-ttu-id="e0868-123">Chame [IPropData:: HrSetPropAccess](ipropdata-hrsetpropaccess.md) para definir o nível de acesso de volta para o IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="e0868-123">Call [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) to set the access level back to IPROP_CLEAN.</span></span> 
    
   - <span data-ttu-id="e0868-124">Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps do objeto de dados da propriedade para recuperar a propriedade alterada e atualizá-lo chamando [IMAPIProp::](imapiprop-setprops.md)SetProps.</span><span class="sxs-lookup"><span data-stu-id="e0868-124">Call the property data object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the changed property and update it by calling [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
5. <span data-ttu-id="e0868-125">Se o nível de acesso ainda for IPROP_CLEAN, o controle não foi modificado.</span><span class="sxs-lookup"><span data-stu-id="e0868-125">If the access level is still IPROP_CLEAN, the control has not been modified.</span></span> 
    
<span data-ttu-id="e0868-126">Para obter mais informações sobre como criar tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e0868-126">For more information about creating display tables, see [Display Tables](display-tables.md).</span></span>
  

