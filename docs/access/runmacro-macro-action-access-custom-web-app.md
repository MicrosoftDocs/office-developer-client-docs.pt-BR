---
title: Ação da macro RunMacro (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Você pode usar a ação ExecutarMacro para executar uma macro de interface do usuário (UI).
ms.openlocfilehash: 98e3b17a6c64fa12ac37e4551d45714c873f5ccb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438439"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="8af87-103">Ação da macro RunMacro (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="8af87-103">RunMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="8af87-104">Você pode usar a ação **ExecutarMacro** para executar uma macro de interface do usuário (UI).</span><span class="sxs-lookup"><span data-stu-id="8af87-104">You can use the **RunMacro** action to run a user interface (UI) macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8af87-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="8af87-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="8af87-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="8af87-107">Setting</span></span>

<span data-ttu-id="8af87-108">A ação **ExecutarMacro** tem os argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="8af87-108">The **RunMacro** action has the following arguments.</span></span> 
  
|<span data-ttu-id="8af87-109">**Argumento da ação**</span><span class="sxs-lookup"><span data-stu-id="8af87-109">**Action argument**</span></span>|<span data-ttu-id="8af87-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8af87-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8af87-111">**Macro Name**</span><span class="sxs-lookup"><span data-stu-id="8af87-111">**Macro Name**</span></span> <br/> |<span data-ttu-id="8af87-112">O nome da macro da interface do usuário a ser executada.</span><span class="sxs-lookup"><span data-stu-id="8af87-112">The name of the UI macro to run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8af87-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8af87-113">Remarks</span></span>

<span data-ttu-id="8af87-114">Ao executar uma macro de interface do usuário contendo a ação **ExecutarMacro** e ela alcançar a ação **ExecutarMacro** , o Access executa a macro chamada interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8af87-114">When you run a UI macro containing the **RunMacro** action, and it reaches the **RunMacro** action, Access runs the called UI macro.</span></span> <span data-ttu-id="8af87-115">Quando a macro de interface do usuário chamada tiver sido concluída, o Access retornará à macro da interface do usuário original e executará a próxima ação.</span><span class="sxs-lookup"><span data-stu-id="8af87-115">When the called UI macro has finished, Access returns to the original UI macro and runs the next action.</span></span> 
  

