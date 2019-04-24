---
title: Exibir a implementação da tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339946"
---
# <a name="display-table-implementation"></a><span data-ttu-id="58cef-103">Exibir a implementação da tabela</span><span class="sxs-lookup"><span data-stu-id="58cef-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="58cef-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58cef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58cef-105">Uma tabela de exibição é usada para mostrar uma folha de propriedades, uma caixa de diálogo especial que é composta de uma ou mais páginas de propriedades com guias dedicadas para exibir e possivelmente editar uma ou mais propriedades.</span><span class="sxs-lookup"><span data-stu-id="58cef-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="58cef-106">Associado a cada tabela de exibição é uma implementação de interface [IAttach: IMAPIProp](iattachimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="58cef-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="58cef-107">A implementação do [IMAPIProp](imapipropiunknown.md) mantém os dados de propriedade apresentados na folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="58cef-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="58cef-108">As linhas em uma tabela de exibição representam os controles na folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="58cef-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="58cef-109">A maioria dos controles pode ser associada às propriedades mantidas com a implementação **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="58cef-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="58cef-110">Quando um usuário altera o valor de um controle modificável, a propriedade correspondente é atualizada.</span><span class="sxs-lookup"><span data-stu-id="58cef-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="58cef-111">As colunas em uma tabela de exibição representam as propriedades do controle, como sua posição na folha de propriedades, o tipo, a estrutura associada e o identificador.</span><span class="sxs-lookup"><span data-stu-id="58cef-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="58cef-112">Para obter uma lista completa das colunas de exibição obrigatórias da tabela, confira [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="58cef-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="58cef-113">MAPI exibe uma folha de propriedades para o usuário de um aplicativo cliente lendo valores de propriedade da implementação **IMAPIProp** associada à tabela de exibição ou a partir da tabela de exibição diretamente.</span><span class="sxs-lookup"><span data-stu-id="58cef-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="58cef-114">Como o usuário trabalha com a folha de propriedades, alterando os valores nos controles, MAPI chama [IMAPIProp::](imapiprop-setprops.md) SetProps para salvar um controle alterado se o sinalizador DT_SET_IMMEDIATE do controle estiver definido.</span><span class="sxs-lookup"><span data-stu-id="58cef-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="58cef-115">Para controles sem o sinalizador DT_SET_IMMEDIATE definido, as alterações nas propriedades são salvas quando o usuário ignora a caixa de diálogo clicando no botão **OK** ou **aplicar agora** .</span><span class="sxs-lookup"><span data-stu-id="58cef-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="58cef-116">Quando um desses botões ou o botão **Cancelar** é clicado, MAPI remove a folha de propriedades do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="58cef-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="58cef-117">O MAPI obtém acesso à sua tabela de exibição chamando o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) na implementação **IMAPIProp** e solicitando a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) ou herdando-a em um chamada que você fez para MAPI, como [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md).</span><span class="sxs-lookup"><span data-stu-id="58cef-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="58cef-118">A primeira técnica de acesso é usada quando os provedores de catálogos de endereços são solicitados a mostrar detalhes sobre usuários de mensagens ou listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="58cef-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="58cef-119">O seguinte processamento ocorre:</span><span class="sxs-lookup"><span data-stu-id="58cef-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="58cef-120">Um cliente chama o método [IAddrBook::D etails](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="58cef-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="58cef-121">MAPI chama o método [IABLogon:: OpenEntry](iablogon-openentry.md) do provedor de catálogo de endereços para acessar o usuário de mensagens que representa a entrada selecionada.</span><span class="sxs-lookup"><span data-stu-id="58cef-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="58cef-122">MAPI chama o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do usuário de mensagens para recuperar a propriedade **PR_DETAILS_TABLE** , a tabela de exibição da caixa de diálogo detalhes.</span><span class="sxs-lookup"><span data-stu-id="58cef-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="58cef-123">MAPI exibe a caixa de diálogo, manipulando a interação do usuário com as informações e a remove quando o usuário tiver concluído.</span><span class="sxs-lookup"><span data-stu-id="58cef-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="58cef-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="58cef-124">See also</span></span>



[<span data-ttu-id="58cef-125">Provedores de serviço MAPI</span><span class="sxs-lookup"><span data-stu-id="58cef-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

