---
title: Implementação da tabela de exibição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3e31dd7b25b3abf333505c8bde57f61be7a10901
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580604"
---
# <a name="display-table-implementation"></a><span data-ttu-id="1259d-103">Implementação da tabela de exibição</span><span class="sxs-lookup"><span data-stu-id="1259d-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="1259d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1259d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1259d-105">Uma tabela de exibição é usada para mostrar uma folha de propriedades, uma caixa de diálogo especial é composta de um ou mais páginas com guias Propriedade dedicada ao exibindo e editando possivelmente uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="1259d-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="1259d-106">Associados com cada exibição tabela é um [IAttach: IMAPIProp](iattachimapiprop.md) implementação de interface.</span><span class="sxs-lookup"><span data-stu-id="1259d-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="1259d-107">A implementação de [IMAPIProp](imapipropiunknown.md) mantém os dados de propriedade apresentada na folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1259d-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="1259d-108">As linhas em uma tabela de exibição representam os controles na folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1259d-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="1259d-109">A maioria dos controles pode ser associado com propriedades mantidas com a implementação de **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="1259d-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="1259d-110">Quando um usuário altera o valor de um controle modificável, a propriedade correspondente é atualizada.</span><span class="sxs-lookup"><span data-stu-id="1259d-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="1259d-111">As colunas em uma tabela de exibição representam as propriedades do controle, como sua posição na folha de propriedades, seu tipo, estrutura associada e identificador.</span><span class="sxs-lookup"><span data-stu-id="1259d-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="1259d-112">Para obter uma lista completa das colunas da tabela de exibição necessários, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1259d-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="1259d-113">MAPI exibe uma folha de propriedades para o usuário de um aplicativo cliente lendo valores de propriedade da implementação **IMAPIProp** associado à tabela de exibição ou da tabela de exibição diretamente.</span><span class="sxs-lookup"><span data-stu-id="1259d-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="1259d-114">Conforme o usuário trabalha com a folha de propriedades, alterando os valores nos controles, MAPI chama [IMAPIProp::SetProps](imapiprop-setprops.md) para salvar um controle alterado se o sinalizador DT_SET_IMMEDIATE do controle está definido.</span><span class="sxs-lookup"><span data-stu-id="1259d-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="1259d-115">Para controles sem o DT_SET_IMMEDIATE sinalizador definido, as alterações nas propriedades são salvas quando o usuário descarte a caixa de diálogo clicando no botão **Okey** ou **Aplicar agora** .</span><span class="sxs-lookup"><span data-stu-id="1259d-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="1259d-116">Quando um desses botões ou o botão **Cancelar** é clicado, MAPI remove a folha de propriedades da exibição.</span><span class="sxs-lookup"><span data-stu-id="1259d-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="1259d-117">MAPI obtém acesso à sua tabela de exibição chamando o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) na implementação **IMAPIProp** e solicitar a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) ou herdando-lo em um chamadas feitas para MAPI, como [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span><span class="sxs-lookup"><span data-stu-id="1259d-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="1259d-118">A primeira técnica de acesso é usada quando os provedores de catálogo de endereços serão solicitadas que deseja mostrar detalhes sobre as mensagens de usuários ou listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="1259d-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="1259d-119">O processamento seguinte ocorre:</span><span class="sxs-lookup"><span data-stu-id="1259d-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="1259d-120">Um cliente chama o método [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="1259d-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="1259d-121">MAPI chama o método de [IABLogon::OpenEntry](iablogon-openentry.md) do provedor catálogo de endereços para acessar o usuário de mensagens que representa a entrada selecionada.</span><span class="sxs-lookup"><span data-stu-id="1259d-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="1259d-122">MAPI chama o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de mensagens do usuário para recuperar a propriedade **PR_DETAILS_TABLE** , a tabela de exibição para a caixa de diálogo detalhes.</span><span class="sxs-lookup"><span data-stu-id="1259d-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="1259d-123">MAPI exibe a caixa de diálogo tratando a interação do usuário com as informações e remove-lo quando o usuário tiver terminado.</span><span class="sxs-lookup"><span data-stu-id="1259d-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1259d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1259d-124">See also</span></span>



[<span data-ttu-id="1259d-125">Provedores de serviços MAPI</span><span class="sxs-lookup"><span data-stu-id="1259d-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

