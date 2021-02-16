---
title: Criando um perfil usando o Assistente de Perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a93cfb05d8abfffc9f55a7ea48efc3c3451dddbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411733"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="7678d-103">Criando um perfil usando o Assistente de Perfil</span><span class="sxs-lookup"><span data-stu-id="7678d-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="7678d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7678d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7678d-105">O Assistente de Perfil é um recurso MAPI que permite que um usuário crie um perfil da maneira mais fácil possível.</span><span class="sxs-lookup"><span data-stu-id="7678d-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="7678d-106">O Assistente de Perfil exibe uma série de caixas de diálogo que solicitam que o usuário selecione serviços de mensagem e insira valores para algumas das propriedades de configuração mais essenciais.</span><span class="sxs-lookup"><span data-stu-id="7678d-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="7678d-107">Para a maioria das outras propriedades necessárias, o Assistente de Perfil usa valores padrão fornecidos.</span><span class="sxs-lookup"><span data-stu-id="7678d-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="7678d-108">Para invocar o Assistente de Perfil, chame **LaunchWizard**, uma função baseada no [protótipo LAUNCHWIZARDENTRY.](launchwizardentry.md)</span><span class="sxs-lookup"><span data-stu-id="7678d-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="7678d-109">O usuário pode adicionar apenas esses serviços de mensagem e provedores de serviços ao novo perfil que dá suporte ao Assistente de Perfil.</span><span class="sxs-lookup"><span data-stu-id="7678d-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="7678d-110">Como cada serviço de mensagens pode exigir que mais propriedades sejam definidas do que o Assistente de Perfil pode manipular, esteja ciente de que, se você usar essa abordagem, é possível que um ou mais dos serviços ou provedores selecionados sejam configurados de forma incompleta.</span><span class="sxs-lookup"><span data-stu-id="7678d-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

