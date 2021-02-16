---
title: Implementação da tabela de exibição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435261"
---
# <a name="display-table-implementation"></a><span data-ttu-id="038b3-103">Implementação da tabela de exibição</span><span class="sxs-lookup"><span data-stu-id="038b3-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="038b3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="038b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="038b3-105">Uma tabela de exibição é usada para mostrar uma folha de propriedades, uma caixa de diálogo especial composta por uma ou mais páginas de propriedades com guias dedicadas à exibição e possivelmente edição de uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="038b3-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="038b3-106">Associado a cada tabela de exibição é uma implementação de interface [IAttach : IMAPIProp.](iattachimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="038b3-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="038b3-107">A [implementação de IMAPIProp](imapipropiunknown.md) mantém os dados de propriedade apresentados na folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="038b3-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="038b3-108">As linhas em uma tabela de exibição representam os controles na folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="038b3-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="038b3-109">A maioria dos controles pode ser associada a propriedades mantidas com a **implementação IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="038b3-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="038b3-110">Quando um usuário altera o valor de um controle modificável, a propriedade correspondente é atualizada.</span><span class="sxs-lookup"><span data-stu-id="038b3-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="038b3-111">As colunas em uma tabela de exibição representam propriedades do controle, como sua posição na folha de propriedades, seu tipo, estrutura associada e identificador.</span><span class="sxs-lookup"><span data-stu-id="038b3-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="038b3-112">Para uma lista completa das colunas de tabela de exibição necessárias, consulte [Tabelas de Exibição.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="038b3-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="038b3-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span><span class="sxs-lookup"><span data-stu-id="038b3-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="038b3-114">Conforme o usuário trabalha com a folha de propriedades, alterando valores nos controles, MAPI chama [IMAPIProp::SetProps](imapiprop-setprops.md) para salvar um controle alterado se o sinalizador DT_SET_IMMEDIATE do controle estiver definido.</span><span class="sxs-lookup"><span data-stu-id="038b3-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="038b3-115">Para controles sem o DT_SET_IMMEDIATE sinalizador definido, as alterações nas propriedades são salvas quando o usuário descarta a caixa de diálogo clicando no **botão OK** ou Aplicar **Agora.**</span><span class="sxs-lookup"><span data-stu-id="038b3-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="038b3-116">Quando um desses botões ou o **botão Cancelar** é clicado, MAPI remove a folha de propriedades da exibição.</span><span class="sxs-lookup"><span data-stu-id="038b3-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="038b3-117">MAPI obtém acesso à sua tabela de exibição chamando o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) na implementação **IMAPIProp** e solicitando a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) ou herdando-a em uma chamada que você fez para MAPI, como [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md).</span><span class="sxs-lookup"><span data-stu-id="038b3-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="038b3-118">A primeira técnica de acesso é usada quando os provedores de agendamento de endereço são solicitados a mostrar detalhes sobre usuários de mensagens ou listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="038b3-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="038b3-119">Ocorre o seguinte processamento:</span><span class="sxs-lookup"><span data-stu-id="038b3-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="038b3-120">Um cliente chama o [método IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="038b3-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="038b3-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span><span class="sxs-lookup"><span data-stu-id="038b3-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="038b3-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span><span class="sxs-lookup"><span data-stu-id="038b3-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="038b3-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span><span class="sxs-lookup"><span data-stu-id="038b3-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="038b3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="038b3-124">See also</span></span>



[<span data-ttu-id="038b3-125">Provedores de Serviços MAPI</span><span class="sxs-lookup"><span data-stu-id="038b3-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

