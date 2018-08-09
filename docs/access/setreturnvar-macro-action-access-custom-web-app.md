---
title: Ação de SetReturnVar Macro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: A ação SetReturnVar cria uma variável de retorno e o configura para um valor específico.
ms.openlocfilehash: d0638c8f1e3b184a7c685ad8649c8923bdfd8f50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765250"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a><span data-ttu-id="2749a-103">Ação de SetReturnVar Macro (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="2749a-103">SetReturnVar Macro action (Access custom web app)</span></span>

<span data-ttu-id="2749a-104">A ação **SetReturnVar** cria uma variável de retorno e o configura para um valor específico.</span><span class="sxs-lookup"><span data-stu-id="2749a-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="2749a-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="2749a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2749a-107">A ação de **SetReturnVar** está disponível somente em Macros de dados.</span><span class="sxs-lookup"><span data-stu-id="2749a-107">The **SetReturnVar** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="2749a-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="2749a-108">Setting</span></span>

<span data-ttu-id="2749a-109">A ação **SetReturnVar** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="2749a-109">The **SetReturnVar** action has the following arguments.</span></span> 
  
|<span data-ttu-id="2749a-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="2749a-110">**Argument name**</span></span>|<span data-ttu-id="2749a-111">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="2749a-111">**Required**</span></span>|<span data-ttu-id="2749a-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2749a-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2749a-113">_Name_</span><span class="sxs-lookup"><span data-stu-id="2749a-113">_Name_</span></span> <br/> |<span data-ttu-id="2749a-114">Sim</span><span class="sxs-lookup"><span data-stu-id="2749a-114">Yes</span></span>  <br/> |<span data-ttu-id="2749a-115">Uma cadeia de caracteres que especifica o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="2749a-115">A string that specifies the name of the variable.</span></span>  <br/> |
| <span data-ttu-id="2749a-116">_Expression_</span><span class="sxs-lookup"><span data-stu-id="2749a-116">_Expression_</span></span> <br/> |<span data-ttu-id="2749a-117">Sim</span><span class="sxs-lookup"><span data-stu-id="2749a-117">Yes</span></span>  <br/> |<span data-ttu-id="2749a-118">Uma expressão que será usada para definir o valor dessa variável temporária.</span><span class="sxs-lookup"><span data-stu-id="2749a-118">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="2749a-119">Não preceda a expressão com o sinal de igual (=).</span><span class="sxs-lookup"><span data-stu-id="2749a-119">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="2749a-120">Você pode clicar no botão **Construir** para usar o **Construtor de expressões** para definir este argumento.</span><span class="sxs-lookup"><span data-stu-id="2749a-120">You can click the **Build** button to use the **Expression Builder** to set this argument.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2749a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2749a-121">Remarks</span></span>

<span data-ttu-id="2749a-122">A ação **SetReturnVar** é usada para criar um **ReturnVar**, que é a variável que pode ser usado por macros que chamar uma macro de dados usando a ação **ExecutarMacrodeDados** .</span><span class="sxs-lookup"><span data-stu-id="2749a-122">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span> 
  
<span data-ttu-id="2749a-123">Depois que um **ReturnVar** é criado pela ação **SetReturnVar** , a macro chamada pode ser usada em uma expressão.</span><span class="sxs-lookup"><span data-stu-id="2749a-123">After a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="2749a-124">Por exemplo, se você criou um **ReturnVar** chamado **UpdateSuccess**, você poderia usar a variável usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="2749a-124">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>
  
`=[ReturnVars]![UpdateSuccess]`

<span data-ttu-id="2749a-125">A ação **SetReturnVar** pode ser usada somente em macros de dados nomeada.</span><span class="sxs-lookup"><span data-stu-id="2749a-125">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="2749a-126">Ele não está disponível em macros de dados que estejam anexadas a um evento de macro de dados.</span><span class="sxs-lookup"><span data-stu-id="2749a-126">It is not available in data macros that are attached to a data macro event.</span></span> 
  

