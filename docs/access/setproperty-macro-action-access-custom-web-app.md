---
title: Ação de macro SetProperty (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Você pode usar a ação setProperty para definir uma propriedade para um controle em um modo de exibição.
ms.openlocfilehash: 1876be32606d66e0570c9e69206a508b8888b157
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307886"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a><span data-ttu-id="31e22-103">Ação de macro SetProperty (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="31e22-103">SetProperty Macro Action (Access custom web app)</span></span>

<span data-ttu-id="31e22-104">Você pode usar a \*\*\*\* ação setProperty para definir uma propriedade para um controle em um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="31e22-104">You can use the **SetProperty** action to set a property for a control on a view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="31e22-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="31e22-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="31e22-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="31e22-107">Setting</span></span>

<span data-ttu-id="31e22-108">A \*\*\*\* ação setProperty tem os argumentos listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="31e22-108">The **SetProperty** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="31e22-109">**Argumento da ação**</span><span class="sxs-lookup"><span data-stu-id="31e22-109">**Action argument**</span></span>|<span data-ttu-id="31e22-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="31e22-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="31e22-111">_Nome do Controle_</span><span class="sxs-lookup"><span data-stu-id="31e22-111">_Control Name_</span></span> <br/> |<span data-ttu-id="31e22-112">Digite o nome do campo ou do controle para o qual você deseja definir o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="31e22-112">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="31e22-113">Deixe este argumento em branco para definir a propriedade para o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="31e22-113">Leave this argument blank to set the property for the view.</span></span>  <br/> |
| <span data-ttu-id="31e22-114">_Property_</span><span class="sxs-lookup"><span data-stu-id="31e22-114">_Property_</span></span> <br/> |<span data-ttu-id="31e22-p103">Selecione a propriedade a ser definida. Consulte a seção **Comentários** deste artigo para obter uma lista das propriedades que podem ser definidas com esta ação.</span><span class="sxs-lookup"><span data-stu-id="31e22-p103">Select the property that you want to set. See the **Remarks** section in this article for a list of the properties that can be set by using this action.  </span></span><br/> |
| <span data-ttu-id="31e22-117">_Valor_</span><span class="sxs-lookup"><span data-stu-id="31e22-117">_Value_</span></span> <br/> |<span data-ttu-id="31e22-p104">Digite o valor com o qual a propriedade deve ser definida. Para propriedades cujos valores sejam Sim ou Não, use **-1** para Sim e **0** para Não.</span><span class="sxs-lookup"><span data-stu-id="31e22-p104">Type the value that the property is to be set to. For properties whose values are either Yes or No, use **-1** for Yes and **0** for No.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="31e22-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="31e22-120">Remarks</span></span>

<span data-ttu-id="31e22-121">Você pode usar a \*\*\*\* ação setProperty para definir as seguintes propriedades de um controle:</span><span class="sxs-lookup"><span data-stu-id="31e22-121">You can use the **SetProperty** action to set the following properties of a control:</span></span> 
  
- <span data-ttu-id="31e22-122">Legenda</span><span class="sxs-lookup"><span data-stu-id="31e22-122">Caption</span></span>
    
- <span data-ttu-id="31e22-123">Habilitado</span><span class="sxs-lookup"><span data-stu-id="31e22-123">Enabled</span></span>
    
- <span data-ttu-id="31e22-124">ForeColor</span><span class="sxs-lookup"><span data-stu-id="31e22-124">ForeColor</span></span>
    
- <span data-ttu-id="31e22-125">Valor</span><span class="sxs-lookup"><span data-stu-id="31e22-125">Value</span></span>
    
- <span data-ttu-id="31e22-126">Visível</span><span class="sxs-lookup"><span data-stu-id="31e22-126">Visible</span></span>
    
<span data-ttu-id="31e22-127">Se você inserir um valor inválido para o argumento \*\* *Valor* \*\*, não ocorrerá nenhum erro, mas o Access poderá alterar a propriedade para um valor diferente, dependendo da forma como o Access interpretar o argumento.</span><span class="sxs-lookup"><span data-stu-id="31e22-127">If you enter an invalid value for the \*\* *Value* \*\* argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span> 
  

