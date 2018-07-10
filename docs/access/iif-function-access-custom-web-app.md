---
title: Função IIf (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Verifica se uma condição for atendida e retorna um valor se for TRUE, de um outro se for FALSE.
ms.openlocfilehash: 26240735341a316a3aed08a12c42e8b6e7af805f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765048"
---
# <a name="iif-function-access-custom-web-app"></a><span data-ttu-id="7c5ed-103">Função IIf (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="7c5ed-103">IIf function (Access custom web app)</span></span>

<span data-ttu-id="7c5ed-104">Verifica se uma condição for atendida e retorna um valor se for TRUE, de um outro se for FALSE.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-104">Checks whether a condition is met, and returns one value if TRUE of another on if it is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="7c5ed-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7c5ed-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c5ed-107">Syntax</span></span>

<span data-ttu-id="7c5ed-108">**IIf** (*Condição*, *TrueValue*, *FalseValue*)</span><span class="sxs-lookup"><span data-stu-id="7c5ed-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span></span> 
  
<span data-ttu-id="7c5ed-109">A função **IIf** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-109">The **IIf** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="7c5ed-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="7c5ed-110">**Argument name**</span></span>|<span data-ttu-id="7c5ed-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7c5ed-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7c5ed-112">*Condição*</span><span class="sxs-lookup"><span data-stu-id="7c5ed-112">*Condition*</span></span>  <br/> |<span data-ttu-id="7c5ed-113">A expressão que você deseja avaliar.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-113">The expression that you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="7c5ed-114">*TrueValue*</span><span class="sxs-lookup"><span data-stu-id="7c5ed-114">*TrueValue*</span></span>  <br/> |<span data-ttu-id="7c5ed-115">Expressão ou valor retornado se a *condição* for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-115">Value or expression returned if  *Condition*  is True.</span></span>  <br/> |
| <span data-ttu-id="7c5ed-116">*FalseValue*</span><span class="sxs-lookup"><span data-stu-id="7c5ed-116">*FalseValue*</span></span>  <br/> |<span data-ttu-id="7c5ed-117">Expressão ou valor retornado se a *condição* for False.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-117">Value or expression returned if  *Condition*  is False.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="7c5ed-118">Example</span><span class="sxs-lookup"><span data-stu-id="7c5ed-118">Example</span></span>

<span data-ttu-id="7c5ed-119">A expressão a seguir pode ser usada para exibir o nome completo de uma pessoa em um dos campos da tabela Nome, Sobrenome e Nome do Meio.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="7c5ed-120">Se o campo MiddleInitial estiver vazio, somente os campos FirstName e LastName são combinados para exibir o nome completo.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


