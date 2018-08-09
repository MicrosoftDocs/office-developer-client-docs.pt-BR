---
title: Ação de Macro ExecutarMacrodeDados (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Você pode usar a ação ExecutarMacrodeDados para executar uma macro de dados independentes.
ms.openlocfilehash: 55a0ff4c731dc517c5d71aa20d8e46c3b4ff4611
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765218"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a><span data-ttu-id="858c0-103">Ação de Macro ExecutarMacrodeDados (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="858c0-103">RunDataMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="858c0-104">Você pode usar a ação **ExecutarMacrodeDados** para executar uma macro de dados independentes.</span><span class="sxs-lookup"><span data-stu-id="858c0-104">You can use the **RunDataMacro** action to run a standalone data macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="858c0-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="858c0-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="858c0-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="858c0-107">Setting</span></span>

<span data-ttu-id="858c0-108">A ação **ExecutarMacrodeDados** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="858c0-108">The **RunDataMacro** action has the following argument.</span></span> 
  
|<span data-ttu-id="858c0-109">**Argumento da ação**</span><span class="sxs-lookup"><span data-stu-id="858c0-109">**Action argument**</span></span>|<span data-ttu-id="858c0-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="858c0-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="858c0-111">_Macro Name_</span><span class="sxs-lookup"><span data-stu-id="858c0-111">_Macro Name_</span></span> <br/> |<span data-ttu-id="858c0-112">O nome da macro de dados a ser executada.</span><span class="sxs-lookup"><span data-stu-id="858c0-112">The name of the data macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="858c0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="858c0-113">Remarks</span></span>

<span data-ttu-id="858c0-114">Quando você selecionar a macro de dados que deseja executar no designer de macros, o Access determinará se a macro de dados exige parâmetros.</span><span class="sxs-lookup"><span data-stu-id="858c0-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="858c0-115">Se a macro de dados requer parâmetros, caixas de texto aparecem onde você pode digitar nos argumentos.</span><span class="sxs-lookup"><span data-stu-id="858c0-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>
  
<span data-ttu-id="858c0-p103">Quando você executa uma macro que contém a ação **ExecutarMacrodeDados** e ela alcançar a ação **ExecutarMacrodeDados**, o Access executará a macro de dados chamada. Após a conclusão da macro de dados chamada, o Access retornará à macro original e executará a próxima ação.</span><span class="sxs-lookup"><span data-stu-id="858c0-p103">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span> 
  

