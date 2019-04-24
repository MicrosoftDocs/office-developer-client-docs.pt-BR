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
ms.openlocfilehash: 951a1c88d2fd4291ee0b48924de6eda8f43c3e47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351342"
---
# <a name="mapi-forms"></a><span data-ttu-id="7635b-103">Formulários MAPI</span><span class="sxs-lookup"><span data-stu-id="7635b-103">MAPI Forms</span></span>

  
  
<span data-ttu-id="7635b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7635b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7635b-105">Após ler esta visão geral da arquitetura de formulários MAPI, você terá uma compreensão do que são formulários MAPI e como eles interagem com outros componentes do subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="7635b-105">After reading this overview of the MAPI form architecture, you will have an understanding of what MAPI forms are and how they interact with other components of the MAPI subsystem.</span></span> <span data-ttu-id="7635b-106">O objetivo desta seção é fornecer o conhecimento conceitual de que você precisa para implementar seus próprios servidores de formulário MAPI.</span><span class="sxs-lookup"><span data-stu-id="7635b-106">The purpose of this section is to give you the conceptual knowledge you need to implement your own MAPI form servers.</span></span>
  
<span data-ttu-id="7635b-107">Antes de ler esta seção, familiarize-se com o material no tópico [visão geral de formulários MAPI](mapi-forms-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="7635b-107">Before reading this section, you should familiarize yourself with the material in the [MAPI Forms Overview](mapi-forms-overview.md) topic.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7635b-108">Como a arquitetura de formulário MAPI é baseada no modelo de objeto de componente (COM), o desenvolvimento de aplicativos de servidor de formulário exige conhecimento de programação COM.</span><span class="sxs-lookup"><span data-stu-id="7635b-108">Because the MAPI form architecture is based on the Component Object Model (COM), developing form server applications requires knowledge of COM programming.</span></span> <span data-ttu-id="7635b-109">Para obter mais informações sobre COM, consulte a seção de serviços de objeto COM e ActiveX no Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7635b-109">For more information about COM, see the COM and ActiveX Object Services section in the Windows SDK.</span></span> 
  

