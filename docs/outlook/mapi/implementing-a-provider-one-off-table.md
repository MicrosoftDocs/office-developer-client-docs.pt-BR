---
title: Implementando uma tabela de One-Off provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436290"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="09de7-103">Implementando uma tabela de One-Off provedor</span><span class="sxs-lookup"><span data-stu-id="09de7-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="09de7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09de7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09de7-105">O MAPI chama o método [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) do provedor quando o usuário de um aplicativo cliente adiciona um destinatário a uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="09de7-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="09de7-106">Normalmente, os tipos de endereços solicitados são exclusivos do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="09de7-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="09de7-107">Se seu provedor oferece suporte à criação de destinatários, ele deve fornecer uma tabela única que expõe modelos para cada tipo de endereço de destinatário com suporte.</span><span class="sxs-lookup"><span data-stu-id="09de7-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="09de7-108">Se o provedor não suportar a criação de destinatários, retorne MAPI_E_NO_SUPPORT da **chamada GetOneOffTable.**</span><span class="sxs-lookup"><span data-stu-id="09de7-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="09de7-109">O MAPI normalmente manterá a tabela única do provedor aberta durante a sessão, liberando-a somente quando um cliente chamar o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) do subsistema ou do livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="09de7-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="09de7-110">MapI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span><span class="sxs-lookup"><span data-stu-id="09de7-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="09de7-111">**Para implementar IABLogon::GetOneOffTable**</span><span class="sxs-lookup"><span data-stu-id="09de7-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="09de7-112">Verifique o valor do parâmetro flags,  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="09de7-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="09de7-113">Se o MAPI_UNICODE sinalizador estiver definido e seu provedor não suportar Unicode, falhará e retornará MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="09de7-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="09de7-114">Verifique se a tabela única do provedor já foi criada.</span><span class="sxs-lookup"><span data-stu-id="09de7-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="09de7-115">Como as tabelas one-off são normalmente estáticas, seu provedor nunca precisa passar pelo processo de criação mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="09de7-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="09de7-116">Se uma tabela já existir, retorne um ponteiro para ela.</span><span class="sxs-lookup"><span data-stu-id="09de7-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="09de7-117">Se uma tabela única ainda não existir, chame **CreateTable** para criar uma.</span><span class="sxs-lookup"><span data-stu-id="09de7-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="09de7-118">De definidas as seguintes propriedades para as colunas em suas linhas de tabela:</span><span class="sxs-lookup"><span data-stu-id="09de7-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="09de7-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) para o nome do tipo de destinatário que o modelo pode criar.</span><span class="sxs-lookup"><span data-stu-id="09de7-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="09de7-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para o identificador de entrada para o modelo único.</span><span class="sxs-lookup"><span data-stu-id="09de7-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="09de7-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) para indicar o nível de hierarquia na exibição de tabela única.</span><span class="sxs-lookup"><span data-stu-id="09de7-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="09de7-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) como TRUE para indicar se a linha representa um modelo e FALSE caso contrário.</span><span class="sxs-lookup"><span data-stu-id="09de7-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="09de7-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) para o tipo de endereço criado pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="09de7-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="09de7-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER ou outro valor que indique o tipo de exibição para o modelo.</span><span class="sxs-lookup"><span data-stu-id="09de7-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="09de7-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) para um valor binário exclusivo.</span><span class="sxs-lookup"><span data-stu-id="09de7-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="09de7-126">Chame [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) para modificar a tabela diretamente.</span><span class="sxs-lookup"><span data-stu-id="09de7-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="09de7-127">Chame [ITableData::HrGetView](itabledata-hrgetview.md) para criar uma implementação de interface **IMAPITable** para retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="09de7-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

