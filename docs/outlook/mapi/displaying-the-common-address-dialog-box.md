---
title: Exibir a caixa de diálogo de endereços comuns
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a7b603504956be9ec3066e5ff5e1d5db7d59852a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766453"
---
# <a name="displaying-the-common-address-dialog-box"></a><span data-ttu-id="00a60-103">Exibir a caixa de diálogo de endereços comuns</span><span class="sxs-lookup"><span data-stu-id="00a60-103">Displaying the Common Address Dialog Box</span></span>

  
  
<span data-ttu-id="00a60-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00a60-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00a60-105">A caixa de diálogo de endereço comuns do MAPI pode ser usada para uma variedade de tarefas de endereçamento como construir uma lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="00a60-105">The MAPI common address dialog box can be used for a variety of addressing tasks such as constructing a recipient list.</span></span> <span data-ttu-id="00a60-106">Para exibir esta caixa de diálogo, chame **IAddrBook::Address**.</span><span class="sxs-lookup"><span data-stu-id="00a60-106">To display this dialog box, call **IAddrBook::Address**.</span></span> <span data-ttu-id="00a60-107">Dependendo de qual dos vários parâmetros que você definir e como defini-las, é possível limitar o seu vídeo às entradas de um determinado tipo de um contêiner específico.</span><span class="sxs-lookup"><span data-stu-id="00a60-107">Depending on which of the many parameters you set and how you set them, you can limit your display to entries of a particular type from a particular container.</span></span>
  
 <span data-ttu-id="00a60-108">**Para limitar a caixa de diálogo de endereço para exibindo apenas entradas de catálogo (PAB) particular de endereços**</span><span class="sxs-lookup"><span data-stu-id="00a60-108">**To limit the address dialog box to displaying personal address book (PAB) entries only**</span></span>
  
1. <span data-ttu-id="00a60-109">Chame [IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar o identificador de entrada do PAB.</span><span class="sxs-lookup"><span data-stu-id="00a60-109">Call [IAddrBook::GetPAB](iaddrbook-getpab.md) to retrieve the entry identifier of the PAB.</span></span> 
    
2. <span data-ttu-id="00a60-110">Criar uma restrição de propriedade que usa RELOP_EQ para o membro **relop** da estrutura de [SPropertyRestriction](spropertyrestriction.md) e **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) como o membro **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="00a60-110">Create a property restriction that uses RELOP_EQ for the **relop** member of the [SPropertyRestriction](spropertyrestriction.md) structure and either **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) as the **ulPropTag** member.</span></span> <span data-ttu-id="00a60-111">Se você usar **PR_ENTRYID**, passe o identificador de entrada recuperado do **GetPAB**.</span><span class="sxs-lookup"><span data-stu-id="00a60-111">If you use **PR_ENTRYID**, pass the entry identifier retrieved from **GetPAB**.</span></span> <span data-ttu-id="00a60-112">Se você usar **PR_AB_PROVIDER_ID**, passe o valor incluído no MSPAB. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="00a60-112">If you use **PR_AB_PROVIDER_ID**, pass the value included in the MSPAB.H header file.</span></span> <span data-ttu-id="00a60-113">**PR_AB_PROVIDER_ID** é o identificador exclusivo para o PAB projetado pela MAPI.</span><span class="sxs-lookup"><span data-stu-id="00a60-113">**PR_AB_PROVIDER_ID** is the unique identifier for the PAB designed by MAPI.</span></span> 
    
3. <span data-ttu-id="00a60-114">Chame [IAddrBook::Address](iaddrbook-address.md) com o parâmetro _lpHierRestriction_ apontando para a restrição de propriedade.</span><span class="sxs-lookup"><span data-stu-id="00a60-114">Call [IAddrBook::Address](iaddrbook-address.md) with the  _lpHierRestriction_ parameter pointing to the property restriction.</span></span> 
    

