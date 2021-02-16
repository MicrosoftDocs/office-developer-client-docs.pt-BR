---
title: Ação de macro DefinirVarLocal (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 12444313-1cfa-49ff-89da-3030fe75c13e
description: Use a ação DefinirVarLocal para criar uma variável temporária e defini-la com um valor específico.
ms.openlocfilehash: 2493bc5c908c551e171a8fa7d9eaeea699a04f72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428113"
---
# <a name="setlocalvar-macro-action-access-custom-web-app"></a><span data-ttu-id="c936f-103">Ação de macro DefinirVarLocal (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="c936f-103">SetLocalVar Macro Action (Access custom web app)</span></span>

<span data-ttu-id="c936f-104">Use a ação **DefinirVarLocal** para criar uma variável temporária e defini-la com um valor específico.</span><span class="sxs-lookup"><span data-stu-id="c936f-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="c936f-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="c936f-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c936f-107">A **ação DefinirVarLocal** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="c936f-107">The **SetLocalVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="c936f-108">Definição</span><span class="sxs-lookup"><span data-stu-id="c936f-108">Setting</span></span>

<span data-ttu-id="c936f-109">A ação **DefinirVarLocal** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c936f-109">The **SetLocalVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="c936f-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="c936f-110">**Argument name**</span></span>|<span data-ttu-id="c936f-111">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c936f-111">**Required**</span></span>|<span data-ttu-id="c936f-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c936f-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c936f-113">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c936f-113">**Name**</span></span> <br/> |<span data-ttu-id="c936f-114">Sim</span><span class="sxs-lookup"><span data-stu-id="c936f-114">Yes</span></span>  <br/> |<span data-ttu-id="c936f-115">Uma cadeia de caracteres que especifica o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="c936f-115">A string that specifies the name of the variable.</span></span>  <br/> |
|<span data-ttu-id="c936f-116">**Expressão**.</span><span class="sxs-lookup"><span data-stu-id="c936f-116">**Expression**</span></span> <br/> |<span data-ttu-id="c936f-117">Sim</span><span class="sxs-lookup"><span data-stu-id="c936f-117">Yes</span></span>  <br/> |<span data-ttu-id="c936f-118">Uma expressão que será usada para definir o valor dessa variável temporária.</span><span class="sxs-lookup"><span data-stu-id="c936f-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="c936f-119">Não preceda a expressão com o sinal de igualdade (=).</span><span class="sxs-lookup"><span data-stu-id="c936f-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="c936f-120">Você pode clicar no botão **Build** para usar o **Construtor de Expressões** para definir esse argumento.</span><span class="sxs-lookup"><span data-stu-id="c936f-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   

