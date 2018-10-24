---
title: Exibir a configuração das folhas de propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fa48e97ed25fe1175ffd3a92ac961dcf5bde50b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588353"
---
# <a name="displaying-configuration-property-sheets"></a><span data-ttu-id="770ab-103">Exibir a configuração das folhas de propriedades</span><span class="sxs-lookup"><span data-stu-id="770ab-103">Displaying configuration property sheets</span></span>

<span data-ttu-id="770ab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="770ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="770ab-105">Provedores de transporte usam o método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) para implementar folhas de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="770ab-105">Transport providers use the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to implement configuration property sheets.</span></span> <span data-ttu-id="770ab-106">Ao chamar **DoConfigPropSheet**, o provedor de transporte passa em um ponteiro para uma matriz de propriedades, juntamente com informações sobre como exibi-los.</span><span class="sxs-lookup"><span data-stu-id="770ab-106">When calling **DoConfigPropSheet**, the transport provider passes in a pointer to an array of properties along with information about how to display them.</span></span> <span data-ttu-id="770ab-107">MAPI apresenta as propriedades para o usuário por meio de uma caixa de diálogo padrão.</span><span class="sxs-lookup"><span data-stu-id="770ab-107">MAPI then presents the properties to the user by means of a standard dialog box.</span></span> <span data-ttu-id="770ab-108">Você é altamente encorajado usar esse mecanismo de folha de propriedade ao implementar o seu provedor de transporte devido a vantagem para o usuário de uma interface consistente.</span><span class="sxs-lookup"><span data-stu-id="770ab-108">You are strongly encouraged to use this property sheet mechanism when implementing your transport provider due to the benefit to the user of a consistent interface.</span></span>
  
## <a name="transport-providers"></a><span data-ttu-id="770ab-109">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="770ab-109">Transport providers</span></span>

<span data-ttu-id="770ab-110">Provedores de transporte podem usar a função [BuildDisplayTable](builddisplaytable.md) para simplificar a construção de uma tabela de exibição para uso com **DoConfigPropSheet**.</span><span class="sxs-lookup"><span data-stu-id="770ab-110">Transport providers can use the [BuildDisplayTable](builddisplaytable.md) function to simplify construction of a display table for use with **DoConfigPropSheet**.</span></span> <span data-ttu-id="770ab-111">Provedores de transporte também podem usar a API de folha de propriedade diretamente.</span><span class="sxs-lookup"><span data-stu-id="770ab-111">Transport providers can also use the property sheet API directly.</span></span> <span data-ttu-id="770ab-112">As alterações nas propriedades de buffer, provedores de transporte pode usar a função [CreateIProp](createiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="770ab-112">To buffer changes to the properties, transport providers can use the [CreateIProp](createiprop.md) function.</span></span> <span data-ttu-id="770ab-113">Isso simplifica a manipulação de cancelamentos pelo usuário enquanto o usuário modifica os valores armazenados nas propriedades.</span><span class="sxs-lookup"><span data-stu-id="770ab-113">This simplifies the handling of cancellations by the user while the user modifies the values stored in the properties.</span></span> <span data-ttu-id="770ab-114">Se necessário, um provedor de transporte também pode fornecer uma caixa de diálogo Assistente caixa para simplificar as tarefas de configuração para o usuário.</span><span class="sxs-lookup"><span data-stu-id="770ab-114">If necessary, a transport provider can also provide a wizard dialog box to simplify configuration tasks for the user.</span></span> 
  

