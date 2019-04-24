---
title: Ação de macro Definirvarlocal (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 12444313-1cfa-49ff-89da-3030fe75c13e
description: Use a ação DefinirVarLocal para criar uma variável temporária e defini-la com um valor específico.
ms.openlocfilehash: 2493bc5c908c551e171a8fa7d9eaeea699a04f72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310932"
---
# <a name="setlocalvar-macro-action-access-custom-web-app"></a><span data-ttu-id="73f37-103">Ação de macro Definirvarlocal (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="73f37-103">SetLocalVar Macro Action (Access custom web app)</span></span>

<span data-ttu-id="73f37-104">Use a ação **DefinirVarLocal** para criar uma variável temporária e defini-la com um valor específico.</span><span class="sxs-lookup"><span data-stu-id="73f37-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="73f37-p101">[!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="73f37-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="73f37-107">A ação **definirvarlocal** está disponível somente em macros de dados.</span><span class="sxs-lookup"><span data-stu-id="73f37-107">The **SetLocalVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="73f37-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="73f37-108">Setting</span></span>

<span data-ttu-id="73f37-109">A ação **DefinirVarLocal** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="73f37-109">The **SetLocalVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="73f37-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="73f37-110">**Argument name**</span></span>|<span data-ttu-id="73f37-111">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="73f37-111">**Required**</span></span>|<span data-ttu-id="73f37-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="73f37-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="73f37-113">**Nome**</span><span class="sxs-lookup"><span data-stu-id="73f37-113">**Name**</span></span> <br/> |<span data-ttu-id="73f37-114">Sim</span><span class="sxs-lookup"><span data-stu-id="73f37-114">Yes</span></span>  <br/> |<span data-ttu-id="73f37-115">Uma cadeia de caracteres que especifica o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="73f37-115">A string that specifies the name of the variable.</span></span>  <br/> |
|<span data-ttu-id="73f37-116">**Expressão**.</span><span class="sxs-lookup"><span data-stu-id="73f37-116">**Expression**</span></span> <br/> |<span data-ttu-id="73f37-117">Sim</span><span class="sxs-lookup"><span data-stu-id="73f37-117">Yes</span></span>  <br/> |<span data-ttu-id="73f37-118">Uma expressão que será usada para definir o valor dessa variável temporária.</span><span class="sxs-lookup"><span data-stu-id="73f37-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="73f37-119">Não preceda a expressão com o sinal de igualdade (=).</span><span class="sxs-lookup"><span data-stu-id="73f37-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="73f37-120">Você pode clicar no botão **construir** para usar o **Construtor de expressões** para definir esse argumento.</span><span class="sxs-lookup"><span data-stu-id="73f37-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   

