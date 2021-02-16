---
title: Ação de macro ExecutarMacrodeDados (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Você pode usar a ação RunDataMacro para executar uma macro de dados autônoma.
ms.openlocfilehash: 68c0e5a3837039bdab1165e686adb3bdf2a5b6f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439342"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a><span data-ttu-id="f47ff-103">Ação de macro ExecutarMacrodeDados (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="f47ff-103">RunDataMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="f47ff-104">Você pode usar a **ação RunDataMacro** para executar uma macro de dados autônoma.</span><span class="sxs-lookup"><span data-stu-id="f47ff-104">You can use the **RunDataMacro** action to run a standalone data macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="f47ff-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="f47ff-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="f47ff-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="f47ff-107">Setting</span></span>

<span data-ttu-id="f47ff-108">A ação **ExecutarMacrodeDados** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="f47ff-108">The **RunDataMacro** action has the following argument.</span></span> 
  
|<span data-ttu-id="f47ff-109">**Argumento da ação**</span><span class="sxs-lookup"><span data-stu-id="f47ff-109">**Action argument**</span></span>|<span data-ttu-id="f47ff-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f47ff-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f47ff-111">_Macro Name_</span><span class="sxs-lookup"><span data-stu-id="f47ff-111">_Macro Name_</span></span> <br/> |<span data-ttu-id="f47ff-112">O nome da macro de dados a ser executada.</span><span class="sxs-lookup"><span data-stu-id="f47ff-112">The name of the data macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f47ff-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f47ff-113">Remarks</span></span>

<span data-ttu-id="f47ff-114">Quando você selecionar a macro de dados que deseja executar no designer de macros, o Access determinará se a macro de dados exige parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f47ff-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="f47ff-115">Se a macro de dados exigir parâmetros, as caixas de texto aparecerão onde você poderá digitar os argumentos.</span><span class="sxs-lookup"><span data-stu-id="f47ff-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>
  
<span data-ttu-id="f47ff-p103">Quando você executa uma macro que contém a ação **ExecutarMacrodeDados** e ela alcançar a ação **ExecutarMacrodeDados**, o Access executará a macro de dados chamada. Após a conclusão da macro de dados chamada, o Access retornará à macro original e executará a próxima ação.</span><span class="sxs-lookup"><span data-stu-id="f47ff-p103">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span> 
  

