---
title: Função escolha (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Retorna o item no índice especificado a partir de uma lista de valores.
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414113"
---
# <a name="choose-function-access-custom-web-app"></a><span data-ttu-id="be9f5-103">Função escolha (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="be9f5-103">Choose function (Access custom web app)</span></span>

<span data-ttu-id="be9f5-104">Retorna o item no índice especificado a partir de uma lista de valores.</span><span class="sxs-lookup"><span data-stu-id="be9f5-104">Returns the item at the specified index from a list of values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="be9f5-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="be9f5-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="be9f5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be9f5-107">Syntax</span></span>

<span data-ttu-id="be9f5-108">**Escolha** (*IndexNumber*, *Value*, [*Value_n*])</span><span class="sxs-lookup"><span data-stu-id="be9f5-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span></span> 
  
<span data-ttu-id="be9f5-109">A função **escolher** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="be9f5-109">The **Choose** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="be9f5-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="be9f5-110">**Argument name**</span></span>|<span data-ttu-id="be9f5-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="be9f5-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="be9f5-112">*IndexNumber*</span><span class="sxs-lookup"><span data-stu-id="be9f5-112">*IndexNumber*</span></span>  <br/> |<span data-ttu-id="be9f5-113">Uma expressão de inteiro que representa um índice baseado em 1 na lista de itens que a segue.</span><span class="sxs-lookup"><span data-stu-id="be9f5-113">An integer expression that represents a 1-based index into the list of the items following it.</span></span>  <br/> |
| <span data-ttu-id="be9f5-114">*Valor*</span><span class="sxs-lookup"><span data-stu-id="be9f5-114">*Value*</span></span>  <br/> |<span data-ttu-id="be9f5-115">Lista de valores de qualquer tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="be9f5-115">List of values of any data type.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be9f5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="be9f5-116">Remarks</span></span>

<span data-ttu-id="be9f5-117">Se o *IndexNumber* fornecido não for um inteiro, o valor será convertido implicitamente em um inteiro.</span><span class="sxs-lookup"><span data-stu-id="be9f5-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span></span> 
  
<span data-ttu-id="be9f5-118">Se o valor do índice exceder os limites da matriz de valores, **escolha** retornará NULL.</span><span class="sxs-lookup"><span data-stu-id="be9f5-118">If the index value exceeds the bounds of the array of values, **Choose** returns NULL.</span></span> 
  

