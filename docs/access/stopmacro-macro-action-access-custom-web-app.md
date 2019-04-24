---
title: Ação da macro PararMacro (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Você pode usar a ação PararMacro para interromper a macro em execução no momento.
ms.openlocfilehash: 8b80422a297647d556fb4b20cc15fb93e8853466
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311015"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="ebcbb-103">Ação da macro PararMacro (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="ebcbb-103">StopMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="ebcbb-104">Você pode usar a ação **PararMacro** para interromper a macro em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="ebcbb-104">You can use the **StopMacro** action to stop the currently running macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ebcbb-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="ebcbb-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="ebcbb-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="ebcbb-107">Setting</span></span>

<span data-ttu-id="ebcbb-108">A ação **PararMacro** não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="ebcbb-108">The **StopMacro** action doesn't have any arguments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ebcbb-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebcbb-109">Remarks</span></span>

<span data-ttu-id="ebcbb-110">Normalmente, você usa esta ação quando uma condição torna necessário parar a macro.</span><span class="sxs-lookup"><span data-stu-id="ebcbb-110">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="ebcbb-111">Por exemplo, você pode criar uma macro de interface do usuário (UI) que abre um modo de exibição mostrando os totais de pedidos diários da data inserida no modo de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="ebcbb-111">For example, you might create a user interface (UI) macro that opens a view showing the daily order totals for the date entered in the current view.</span></span> <span data-ttu-id="ebcbb-112">Você pode usar uma expressão condicional para ter certeza de que o controle de data da ordem na caixa de diálogo contém uma data válida.</span><span class="sxs-lookup"><span data-stu-id="ebcbb-112">You could use a conditional expression to be sure that the Order Date control on the dialog box contains a valid date.</span></span> <span data-ttu-id="ebcbb-113">Caso contrário, a ação **MessageBox** poderá exibir uma mensagem de erro e a ação **PararMacro** poderá interromper a macro da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="ebcbb-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the UI macro.</span></span> 
  

