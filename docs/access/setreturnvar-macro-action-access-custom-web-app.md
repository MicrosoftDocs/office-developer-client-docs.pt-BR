---
title: Ação de macro SetReturnVar (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: A ação SetReturnVar cria uma variável de retorno e a define como um valor específico.
ms.openlocfilehash: 29445f5021bed99fe45cee1d34457f1f91ca417d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409591"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a><span data-ttu-id="17881-103">Ação de macro SetReturnVar (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="17881-103">SetReturnVar Macro action (Access custom web app)</span></span>

<span data-ttu-id="17881-104">A ação **SetReturnVar** cria uma variável de retorno e a define como um valor específico.</span><span class="sxs-lookup"><span data-stu-id="17881-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="17881-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="17881-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="17881-107">A ação **SetReturnVar** está disponível somente em macros de dados.</span><span class="sxs-lookup"><span data-stu-id="17881-107">The **SetReturnVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="17881-108">Setting</span><span class="sxs-lookup"><span data-stu-id="17881-108">Setting</span></span>

<span data-ttu-id="17881-109">A ação **SetReturnVar** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="17881-109">The **SetReturnVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="17881-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="17881-110">**Argument name**</span></span>|<span data-ttu-id="17881-111">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="17881-111">**Required**</span></span>|<span data-ttu-id="17881-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="17881-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="17881-113">_Nome_</span><span class="sxs-lookup"><span data-stu-id="17881-113">_Name_</span></span> <br/> |<span data-ttu-id="17881-114">Sim</span><span class="sxs-lookup"><span data-stu-id="17881-114">Yes</span></span>  <br/> |<span data-ttu-id="17881-115">Uma cadeia de caracteres que especifica o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="17881-115">A string that specifies the name of the variable.</span></span>  <br/> |
| <span data-ttu-id="17881-116">_Expressão_.</span><span class="sxs-lookup"><span data-stu-id="17881-116">_Expression_</span></span> <br/> |<span data-ttu-id="17881-117">Sim</span><span class="sxs-lookup"><span data-stu-id="17881-117">Yes</span></span>  <br/> |<span data-ttu-id="17881-118">Uma expressão que será usada para definir o valor dessa variável temporária.</span><span class="sxs-lookup"><span data-stu-id="17881-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="17881-119">Não preceda a expressão com o sinal de igualdade (=).</span><span class="sxs-lookup"><span data-stu-id="17881-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="17881-120">Você pode clicar no botão **Build** para usar o **Construtor de Expressões** para definir esse argumento.</span><span class="sxs-lookup"><span data-stu-id="17881-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17881-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="17881-121">Remarks</span></span>

<span data-ttu-id="17881-122">A ação **SetReturnVar** é usada para criar um **ReturnVar**, que é variável que pode ser usada por macros que chamam uma macro de dados usando a ação **RunDataMacro** .</span><span class="sxs-lookup"><span data-stu-id="17881-122">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span> 
  
<span data-ttu-id="17881-123">Depois que um **ReturnVar** é criado pela ação **SetReturnVar** , a macro de chamada pode usá-la em uma expressão.</span><span class="sxs-lookup"><span data-stu-id="17881-123">After a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="17881-124">Por exemplo, se você criou um **ReturnVar** chamado **UpdateSuccess**, poderia usar a variável usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="17881-124">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>
  
`=[ReturnVars]![UpdateSuccess]`

<span data-ttu-id="17881-125">A ação **SetReturnVar** pode ser usada somente em macros de dados nomeadas.</span><span class="sxs-lookup"><span data-stu-id="17881-125">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="17881-126">Ele não está disponível em macros de dados anexadas a um evento de macro de dados.</span><span class="sxs-lookup"><span data-stu-id="17881-126">It is not available in data macros that are attached to a data macro event.</span></span> 
  

