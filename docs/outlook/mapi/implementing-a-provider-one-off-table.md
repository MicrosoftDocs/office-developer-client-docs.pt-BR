---
title: Implementar a tabela única de um provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 99146f93dcf634be6766f5c6fcc0d1c610b84d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767415"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="e3fbc-103">Implementar a tabela única de um provedor</span><span class="sxs-lookup"><span data-stu-id="e3fbc-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="e3fbc-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e3fbc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e3fbc-105">MAPI chama o método de [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) do seu provedor quando o usuário de um aplicativo cliente adiciona um destinatário a uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="e3fbc-106">Normalmente, os tipos de endereços solicitados são exclusivos para seu sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="e3fbc-107">Se seu provedor de suporte para a criação de destinatário, ele deve fornecer uma tabela único que expõe os modelos para cada tipo de endereço do destinatário com suporte.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="e3fbc-108">Se seu provedor não oferece suporte a criação de destinatário, retorne MAPI_E_NO_SUPPORT da chamada **GetOneOffTable** .</span><span class="sxs-lookup"><span data-stu-id="e3fbc-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="e3fbc-109">MAPI normalmente será mantenha tabela únicos do seu provedor aberto para o tempo de vida da sessão, liberá-lo apenas quando um cliente chama do subsistema ou método de [IMAPIStatus::ValidateState](imapistatus-validatestate.md) do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="e3fbc-110">MAPI registra para notificações sobre esta tabela para que se modelos são adicionados ou excluídos, essas alterações podem sejam refletidas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="e3fbc-111">**Para implementar IABLogon:: GetOneOffTable**</span><span class="sxs-lookup"><span data-stu-id="e3fbc-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="e3fbc-112">Verifica o valor do parâmetro flags, _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="e3fbc-113">Se o sinalizador MAPI_UNICODE está definido e o provedor não oferece suporte a Unicode, falhar e retornar MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="e3fbc-114">Verifique se tabela únicos do seu provedor já foi criada.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="e3fbc-115">Como tabelas únicas são geralmente estáticas, seu provedor nunca deve passar o processo de criação mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="e3fbc-116">Se já existir uma tabela, retorne um ponteiro para ele.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="e3fbc-117">Se ainda não existir uma tabela único, chame **CreateTable** para criar um.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="e3fbc-118">Defina as seguintes propriedades para as colunas em suas linhas da tabela:</span><span class="sxs-lookup"><span data-stu-id="e3fbc-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="e3fbc-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome do tipo de destinatário que o modelo pode criar.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="e3fbc-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) para o identificador de entrada para o modelo único.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="e3fbc-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) para indicar o nível de hierarquia na tabela únicas são exibidas.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="e3fbc-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) como TRUE para indicar se a linha representa um modelo e FALSE caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="e3fbc-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) para o tipo de endereço criado pelo modelo.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="e3fbc-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para DT_MAILUSER ou outro valor que indica o tipo de exibição para o modelo.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="e3fbc-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) como um valor binário exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="e3fbc-126">Chame [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) para modificar a tabela diretamente.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="e3fbc-127">Chame [ITableData::HrGetView](itabledata-hrgetview.md) para criar uma implementação de interface **IMAPITable** para retornar ao chamador.</span><span class="sxs-lookup"><span data-stu-id="e3fbc-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

