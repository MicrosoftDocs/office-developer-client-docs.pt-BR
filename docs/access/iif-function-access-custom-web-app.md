---
title: Função IIf (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Verifica se uma condição é atendida e retorna um valor se for verdadeiro de outro em se for FALSE.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301859"
---
# <a name="iif-function-access-custom-web-app"></a><span data-ttu-id="b5016-103">Função IIf (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="b5016-103">IIf function (Access custom web app)</span></span>

<span data-ttu-id="b5016-104">Verifica se uma condição é atendida e retorna um valor se for verdadeiro de outro em se for FALSE.</span><span class="sxs-lookup"><span data-stu-id="b5016-104">Checks whether a condition is met, and returns one value if TRUE of another on if it is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b5016-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="b5016-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b5016-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5016-107">Syntax</span></span>

<span data-ttu-id="b5016-108">**IIF** (*Condição*, *TrueValue*, *FalseValue*)</span><span class="sxs-lookup"><span data-stu-id="b5016-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span></span> 
  
<span data-ttu-id="b5016-109">A função **IIF** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="b5016-109">The **IIf** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="b5016-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="b5016-110">**Argument name**</span></span>|<span data-ttu-id="b5016-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b5016-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b5016-112">*Condition*</span><span class="sxs-lookup"><span data-stu-id="b5016-112">*Condition*</span></span>  <br/> |<span data-ttu-id="b5016-113">A expressão que você deseja avaliar.</span><span class="sxs-lookup"><span data-stu-id="b5016-113">The expression that you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="b5016-114">*TrueValue*</span><span class="sxs-lookup"><span data-stu-id="b5016-114">*TrueValue*</span></span>  <br/> |<span data-ttu-id="b5016-115">Valor ou expressão retornada se *Condition* for true.</span><span class="sxs-lookup"><span data-stu-id="b5016-115">Value or expression returned if  *Condition*  is True.</span></span>  <br/> |
| <span data-ttu-id="b5016-116">*FalseValue*</span><span class="sxs-lookup"><span data-stu-id="b5016-116">*FalseValue*</span></span>  <br/> |<span data-ttu-id="b5016-117">Valor ou expressão retornada se *Condition* for false.</span><span class="sxs-lookup"><span data-stu-id="b5016-117">Value or expression returned if  *Condition*  is False.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="b5016-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b5016-118">Example</span></span>

<span data-ttu-id="b5016-119">A expressão a seguir pode ser usada para exibir o nome completo de uma pessoa quando a tabela contém os campos Nome, Nome do Meio e Sobrenome.</span><span class="sxs-lookup"><span data-stu-id="b5016-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="b5016-120">Se o campo Nome do Meio estiver em branco, apenas os campos de Nome e Sobrenome serão combinados para exibir o nome completo.</span><span class="sxs-lookup"><span data-stu-id="b5016-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


