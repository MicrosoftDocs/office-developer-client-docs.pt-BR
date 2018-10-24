---
title: Formulários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41d35370-495d-40fe-80bc-6c3bfc995b85
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b53cdb4fe379405018555f1cca9fa40ddc5d0fa8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592483"
---
# <a name="mapi-forms"></a><span data-ttu-id="2fe17-103">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="2fe17-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="2fe17-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2fe17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2fe17-105">Após ler esta visão geral da arquitetura do formulário MAPI, você terá uma compreensão de quais são os formulários MAPI e como eles interagem com outros componentes do subsistema de MAPI.</span><span class="sxs-lookup"><span data-stu-id="2fe17-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="2fe17-106">A finalidade desta seção é dar a você o conhecimento conceitual que você precisa implementar seus próprios servidores de formulário MAPI.</span><span class="sxs-lookup"><span data-stu-id="2fe17-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="2fe17-107">Antes de ler esta seção, familiarize-se com o material no tópico [Visão geral dos formulários de MAPI](mapi-forms-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="2fe17-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2fe17-108">Como a arquitetura do MAPI formulário se baseia no modelo COM (Component Object), desenvolvimento de aplicativos de servidor do formulário requer conhecimento de programação COM.</span><span class="sxs-lookup"><span data-stu-id="2fe17-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="2fe17-109">Para obter mais informações sobre o COM, consulte a seção de serviços de objetos ActiveX e COM no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="2fe17-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

