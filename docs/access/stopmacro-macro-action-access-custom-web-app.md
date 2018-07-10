---
title: Ação de Macro PararMacro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Você pode usar a ação PararMacro para interromper a macro em execução no momento.
ms.openlocfilehash: 54501b65eb1847287e810ae43742a2e6e5384264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765229"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="bbd7e-103">Ação de Macro PararMacro (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="bbd7e-103">StopMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="bbd7e-104">Você pode usar a ação **PararMacro** para interromper a macro em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="bbd7e-104">You can use the **StopMacro** action to stop the currently running macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="bbd7e-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="bbd7e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="bbd7e-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="bbd7e-107">Setting</span></span>

<span data-ttu-id="bbd7e-108">A ação **PararMacro** não tem nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="bbd7e-108">The **StopMacro** action doesn't have any arguments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bbd7e-109">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="bbd7e-109">Remarks</span></span>

<span data-ttu-id="bbd7e-110">Geralmente você usa esta ação quando uma condição torna necessário para interromper a macro.</span><span class="sxs-lookup"><span data-stu-id="bbd7e-110">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="bbd7e-111">Por exemplo, você pode criar uma macro (UI) da interface de usuário que abre uma exibição mostrando os totais de ordem de diário para a data inserida na exibição atual.</span><span class="sxs-lookup"><span data-stu-id="bbd7e-111">For example, you might create a user interface (UI) macro that opens a view showing the daily order totals for the date entered in the current view.</span></span> <span data-ttu-id="bbd7e-112">Você poderia usar uma expressão condicional para certificar-se de que o controle de data do pedido na caixa de diálogo contém uma data válida.</span><span class="sxs-lookup"><span data-stu-id="bbd7e-112">You could use a conditional expression to be sure that the Order Date control on the dialog box contains a valid date.</span></span> <span data-ttu-id="bbd7e-113">Caso contrário, a ação **MessageBox** pode exibir uma mensagem de erro e a ação **PararMacro** pode interromper a macro de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="bbd7e-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the UI macro.</span></span> 
  

