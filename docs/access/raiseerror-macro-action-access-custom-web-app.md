---
title: Ação de macro RaiseError (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5e29bf64-300a-4094-82ff-664e79782d86
description: A ação RaiseError exibe uma janela pop-up que contém uma mensagem de erro especificada.
ms.openlocfilehash: 49e544d2234759709c19052b5540d42e88070849
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408240"
---
# <a name="raiseerror-macro-action-access-custom-web-app"></a><span data-ttu-id="8460a-103">Ação de macro RaiseError (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="8460a-103">RaiseError Macro Action (Access custom web app)</span></span>

<span data-ttu-id="8460a-104">A **ação RaiseError** exibe uma janela pop-up que contém uma mensagem de erro especificada.</span><span class="sxs-lookup"><span data-stu-id="8460a-104">The **RaiseError** action displays a popup window that contains a specified error message.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8460a-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="8460a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8460a-107">A ação **GerarErro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="8460a-107">The **RaiseError** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="8460a-108">Setting</span><span class="sxs-lookup"><span data-stu-id="8460a-108">Setting</span></span>

<span data-ttu-id="8460a-109">A **ação RaiseError** tem o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="8460a-109">The **RaiseError** action has the following argument.</span></span> 
  
|<span data-ttu-id="8460a-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="8460a-110">**Argument**</span></span>|<span data-ttu-id="8460a-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8460a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8460a-112">_Descrição do erro_</span><span class="sxs-lookup"><span data-stu-id="8460a-112">_Error Description_</span></span> <br/> |<span data-ttu-id="8460a-113">Uma expressão de cadeia de caracteres que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="8460a-113">A string expression that describes the error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8460a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8460a-114">Remarks</span></span>

<span data-ttu-id="8460a-115">Quando a **ação RaiseError** é chamada, todas as operações na transação atual são re devedas.</span><span class="sxs-lookup"><span data-stu-id="8460a-115">When the **RaiseError** action is called, all of the operations in the current transaction are rolled back.</span></span> 
  

