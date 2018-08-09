---
title: Criar um perfil usando o assistente de perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 29a135264772847a624e1a4558b68bcf822b18df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766349"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="2827a-103">Criar um perfil usando o assistente de perfil</span><span class="sxs-lookup"><span data-stu-id="2827a-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="2827a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2827a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2827a-105">O Assistente de perfil é um recurso MAPI que permite que o usuário crie um perfil da maneira mais fácil de possíveis.</span><span class="sxs-lookup"><span data-stu-id="2827a-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="2827a-106">O Assistente de perfil exibe uma série de caixas de diálogo que solicita ao usuário selecionar serviços de mensagem e insira valores para algumas das propriedades de configuração mais essenciais.</span><span class="sxs-lookup"><span data-stu-id="2827a-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="2827a-107">Para a maioria das outras propriedades necessárias, o Assistente de perfil usa valores padrão fornecidos.</span><span class="sxs-lookup"><span data-stu-id="2827a-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="2827a-108">Para invocar o Assistente de perfil, chame **LaunchWizard**, uma função com base em protótipo [LAUNCHWIZARDENTRY](launchwizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="2827a-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="2827a-109">O usuário pode adicionar apenas os serviços de mensagem e os provedores de serviço para o novo perfil que suportam o Assistente de perfil.</span><span class="sxs-lookup"><span data-stu-id="2827a-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="2827a-110">Como cada serviço de mensagem pode exigir mais de propriedades a ser definido do Assistente de perfil pode manipular, lembre-se de que se você usar essa abordagem, é possível para uma ou mais dos serviços selecionados ou provedores parcialmente ser configurado.</span><span class="sxs-lookup"><span data-stu-id="2827a-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

