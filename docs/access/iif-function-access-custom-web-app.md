---
title: Função IIf (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Verifica se uma condição é atendida e retorna um valor se VERDADEIRO de outro em caso de falso.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439076"
---
# <a name="iif-function-access-custom-web-app"></a><span data-ttu-id="8ceb5-103">Função IIf (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="8ceb5-103">IIf function (Access custom web app)</span></span>

<span data-ttu-id="8ceb5-104">Verifica se uma condição é atendida e retorna um valor se VERDADEIRO de outro em caso de falso.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-104">Checks whether a condition is met, and returns one value if TRUE of another on if it is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="8ceb5-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8ceb5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ceb5-107">Syntax</span></span>

<span data-ttu-id="8ceb5-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span><span class="sxs-lookup"><span data-stu-id="8ceb5-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span></span> 
  
<span data-ttu-id="8ceb5-109">A **função IIf** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-109">The **IIf** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="8ceb5-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="8ceb5-110">**Argument name**</span></span>|<span data-ttu-id="8ceb5-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8ceb5-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8ceb5-112">*Condition*</span><span class="sxs-lookup"><span data-stu-id="8ceb5-112">*Condition*</span></span>  <br/> |<span data-ttu-id="8ceb5-113">A expressão que você deseja avaliar.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-113">The expression that you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="8ceb5-114">*TrueValue*</span><span class="sxs-lookup"><span data-stu-id="8ceb5-114">*TrueValue*</span></span>  <br/> |<span data-ttu-id="8ceb5-115">Valor ou expressão retornado se  *Condição*  for True.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-115">Value or expression returned if  *Condition*  is True.</span></span>  <br/> |
| <span data-ttu-id="8ceb5-116">*FalseValue*</span><span class="sxs-lookup"><span data-stu-id="8ceb5-116">*FalseValue*</span></span>  <br/> |<span data-ttu-id="8ceb5-117">Valor ou expressão retornado se  *Condição*  for False.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-117">Value or expression returned if  *Condition*  is False.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="8ceb5-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8ceb5-118">Example</span></span>

<span data-ttu-id="8ceb5-119">A expressão a seguir pode ser usada para exibir o nome completo de uma pessoa quando a tabela contém os campos Nome, Nome do Meio e Sobrenome.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="8ceb5-120">Se o campo Nome do Meio estiver em branco, apenas os campos de Nome e Sobrenome serão combinados para exibir o nome completo.</span><span class="sxs-lookup"><span data-stu-id="8ceb5-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


