---
title: Ação de Macro ExecutarMacro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Você pode usar a ação ExecutarMacro para executar uma macro (UI) da interface de usuário.
ms.openlocfilehash: 68a59e246c0af8385a17aedcf3da771c720f8fd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765223"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="8704c-103">Ação de Macro ExecutarMacro (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="8704c-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="8704c-104">Você pode usar a ação **ExecutarMacro** para executar uma macro (UI) da interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="8704c-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8704c-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="8704c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="8704c-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="8704c-107">Setting</span></span>

<span data-ttu-id="8704c-108">A ação **ExecutarMacro** tem os argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="8704c-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="8704c-109">**Argumento da ação**</span><span class="sxs-lookup"><span data-stu-id="8704c-109">**Action argument**</span></span>|<span data-ttu-id="8704c-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8704c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8704c-111">**Macro Name**</span><span class="sxs-lookup"><span data-stu-id="8704c-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="8704c-112">O nome da macro a interface do usuário a ser executada.</span><span class="sxs-lookup"><span data-stu-id="8704c-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8704c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8704c-113">Remarks</span></span>

<span data-ttu-id="8704c-114">Quando você executar uma macro de interface do usuário que contém a ação **ExecutarMacro** e alcançar a ação **ExecutarMacro** , o Access executa a macro chamada da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8704c-114">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro.</span></span> <span data-ttu-id="8704c-115">Quando a macro chamada da interface do usuário for concluída, o Access retorna à macro da interface do usuário original e executa a próxima ação.</span><span class="sxs-lookup"><span data-stu-id="8704c-115">When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

