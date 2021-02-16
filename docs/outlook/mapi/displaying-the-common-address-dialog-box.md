---
title: Exibindo a caixa de diálogo Endereço Comum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 812c850d1fcb6d3712d76b160b56b839b2e1353d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436899"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="40a65-103">Exibindo a caixa de diálogo Endereço Comum</span><span class="sxs-lookup"><span data-stu-id="40a65-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="40a65-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40a65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40a65-105">A caixa de diálogo de endereço comum MAPI pode ser usada para uma variedade de tarefas de endereçamento, como a construção de uma lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="40a65-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="40a65-106">Para exibir essa caixa de diálogo, chame **IAddrBook::Address**.</span><span class="sxs-lookup"><span data-stu-id="40a65-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="40a65-107">Dependendo de quais dos muitos parâmetros você definir e de como defini-los, você pode limitar a exibição às entradas de um tipo específico de um contêiner específico.</span><span class="sxs-lookup"><span data-stu-id="40a65-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="40a65-108">**Para limitar a caixa de diálogo de endereço apenas para exibir entradas de PAB (lista de endereços pessoais)**</span><span class="sxs-lookup"><span data-stu-id="40a65-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="40a65-109">Chame [IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar o identificador de entrada do PAB.</span><span class="sxs-lookup"><span data-stu-id="40a65-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="40a65-110">Crie uma restrição de propriedade que use RELOP_EQ para o membro **repropriedade** da estrutura [SPropertyRestriction](spropertyrestriction.md) **e PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) como o membro **ulPropTag.**</span><span class="sxs-lookup"><span data-stu-id="40a65-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="40a65-111">Se você usar **PR_ENTRYID**, passe o identificador de entrada recuperado de **GetPAB**.</span><span class="sxs-lookup"><span data-stu-id="40a65-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="40a65-112">Se você usar **PR_AB_PROVIDER_ID**, passe o valor incluído no MSPAB. Arquivo de header H.</span><span class="sxs-lookup"><span data-stu-id="40a65-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="40a65-113">**PR_AB_PROVIDER_ID** é o identificador exclusivo para o PAB projetado por MAPI.</span><span class="sxs-lookup"><span data-stu-id="40a65-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="40a65-114">Chame [IAddrBook::Address](iaddrbook-address.md) com o  _parâmetro lpHierRestriction_ apontando para a restrição de propriedade.</span><span class="sxs-lookup"><span data-stu-id="40a65-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    

