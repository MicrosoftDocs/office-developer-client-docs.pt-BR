---
title: Ação de Macro DefinirPropriedade (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Você pode usar a ação DefinirPropriedade para definir uma propriedade para um controle em um modo de exibição.
ms.openlocfilehash: 89ac2b10715d707d3b6ee09ee8ab915384c5acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765221"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a><span data-ttu-id="89e13-103">Ação de Macro DefinirPropriedade (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="89e13-103">SetProperty Macro Action (Access custom web app)</span></span>

<span data-ttu-id="89e13-104">Você pode usar a ação **DefinirPropriedade** para definir uma propriedade para um controle em um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="89e13-104">You can use the **SetProperty** action to set a property for a control on a view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="89e13-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="89e13-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="89e13-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="89e13-107">Setting</span></span>

<span data-ttu-id="89e13-108">A ação **DefinirPropriedade** tem os argumentos listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="89e13-108">The **SetProperty** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="89e13-109">**Argumento da ação**</span><span class="sxs-lookup"><span data-stu-id="89e13-109">**Action argument**</span></span>|<span data-ttu-id="89e13-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="89e13-110">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="89e13-111">_Nome do Controle_</span><span class="sxs-lookup"><span data-stu-id="89e13-111">_Control Name_</span></span> <br/> |<span data-ttu-id="89e13-112">Digite o nome do campo ou controle para o qual você deseja definir o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="89e13-112">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="89e13-113">Deixe este argumento em branco para definir a propriedade no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="89e13-113">Leave this argument blank to set the property for the view.</span></span>  <br/> |
| <span data-ttu-id="89e13-114">_Propriedade_</span><span class="sxs-lookup"><span data-stu-id="89e13-114">_Property_</span></span> <br/> |<span data-ttu-id="89e13-p103">Selecione a propriedade a ser definida. Consulte a seção **Comentários** deste artigo para obter uma lista das propriedades que podem ser definidas com esta ação.</span><span class="sxs-lookup"><span data-stu-id="89e13-p103">Select the property that you want to set. See the **Remarks** section in this article for a list of the properties that can be set by using this action.  </span></span><br/> |
| <span data-ttu-id="89e13-117">_Valor_</span><span class="sxs-lookup"><span data-stu-id="89e13-117">_Value_</span></span> <br/> |<span data-ttu-id="89e13-p104">Digite o valor com o qual a propriedade deve ser definida. Para propriedades cujos valores sejam Sim ou Não, use **-1** para Sim e **0** para Não.</span><span class="sxs-lookup"><span data-stu-id="89e13-p104">Type the value that the property is to be set to. For properties whose values are either Yes or No, use **-1** for Yes and **0** for No.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="89e13-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="89e13-120">Remarks</span></span>

<span data-ttu-id="89e13-121">Você pode usar a ação **DefinirPropriedade** para definir as seguintes propriedades de um controle:</span><span class="sxs-lookup"><span data-stu-id="89e13-121">You can use the **SetProperty** action to set the following properties of a control:</span></span> 
  
- <span data-ttu-id="89e13-122">Caption</span><span class="sxs-lookup"><span data-stu-id="89e13-122">Caption</span></span>
    
- <span data-ttu-id="89e13-123">Habilitado</span><span class="sxs-lookup"><span data-stu-id="89e13-123">Enabled</span></span>
    
- <span data-ttu-id="89e13-124">ForeColor</span><span class="sxs-lookup"><span data-stu-id="89e13-124">ForeColor</span></span>
    
- <span data-ttu-id="89e13-125">Value</span><span class="sxs-lookup"><span data-stu-id="89e13-125">Value</span></span>
    
- <span data-ttu-id="89e13-126">Visible</span><span class="sxs-lookup"><span data-stu-id="89e13-126">Visible</span></span>
    
<span data-ttu-id="89e13-127">Se você inserir um valor inválido para o argumento ** *Valor* **, não ocorrerá nenhum erro, mas o Access poderá alterar a propriedade para um valor diferente, dependendo da forma como o Access interpretar o argumento.</span><span class="sxs-lookup"><span data-stu-id="89e13-127">If you enter an invalid value for the ** *Value* ** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span> 
  

