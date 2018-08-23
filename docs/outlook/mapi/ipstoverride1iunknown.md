---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e73115811fe0009769826e0f6a011c489772f770
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569845"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="81138-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81138-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="81138-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81138-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81138-105">Permite que um provedor de armazenamento de arquivo (. PST) de pastas particulares substituir a política de PSTDisableGrow.</span><span class="sxs-lookup"><span data-stu-id="81138-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81138-106">Herda de:</span><span class="sxs-lookup"><span data-stu-id="81138-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="81138-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="81138-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="81138-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="81138-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="81138-109">Provedor de repositórios de PST</span><span class="sxs-lookup"><span data-stu-id="81138-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="81138-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="81138-110">Called by:</span></span>  <br/> |<span data-ttu-id="81138-111">Cliente</span><span class="sxs-lookup"><span data-stu-id="81138-111">Client</span></span>  <br/> |
|<span data-ttu-id="81138-112">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="81138-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="81138-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="81138-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="81138-114">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="81138-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="81138-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="81138-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="81138-116">Recupera a lista dos registros para o arquivo de pastas particulares (. pst).</span><span class="sxs-lookup"><span data-stu-id="81138-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="81138-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="81138-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="81138-118">Registra os arquivos de pastas particulares para desbloqueio automático, evitando mais chamadas para HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="81138-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="81138-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="81138-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="81138-120">Desbloqueia um arquivo de pastas particulares para crescimento.</span><span class="sxs-lookup"><span data-stu-id="81138-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81138-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="81138-121">Remarks</span></span>

<span data-ttu-id="81138-122">Os identificadores de Interface de manipulador substituir PST não poderão ser definidos no arquivo de cabeçalho para download que você possui atualmente, caso em que você irá encontrá-las no tópico [Constantes MAPI](mapi-constants.md) e pode copiar e adicioná-los ao seu código.</span><span class="sxs-lookup"><span data-stu-id="81138-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="81138-123">Use a macro DEFINE_GUID definida no guiddef.h de arquivo de cabeçalho do Software Development Kit (SDK) do Microsoft Windows para associar nomes simbólicos de identificador globalmente exclusivo (GUID) com seus valores.</span><span class="sxs-lookup"><span data-stu-id="81138-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="81138-124">Para obter mais informações, consulte [como implementar um manipulador de substituição de PST para ignorar a política PSTDisableGrow no Outlook 2007](http://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="81138-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="81138-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="81138-125">See also</span></span>



[<span data-ttu-id="81138-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81138-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

