---
title: Escolha a função (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Retorna o item no índice especificado de uma lista de valores.
ms.openlocfilehash: a6db959945bfcfc15993d3979cb9b2b3da0da904
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765066"
---
# <a name="choose-function-access-custom-web-app"></a><span data-ttu-id="ac707-103">Escolha a função (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="ac707-103">Choose function (Access custom web app)</span></span>

<span data-ttu-id="ac707-104">Retorna o item no índice especificado de uma lista de valores.</span><span class="sxs-lookup"><span data-stu-id="ac707-104">Returns the item at the specified index from a list of values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ac707-p101">[!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="ac707-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ac707-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac707-107">Syntax</span></span>

<span data-ttu-id="ac707-108">**Escolha** (*Número_de_índice*, *valor*, [*Value_n*])</span><span class="sxs-lookup"><span data-stu-id="ac707-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span></span> 
  
<span data-ttu-id="ac707-109">A função **Escolher** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="ac707-109">The **Choose** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ac707-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="ac707-110">**Argument name**</span></span>|<span data-ttu-id="ac707-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ac707-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ac707-112">*Número_de_índice*</span><span class="sxs-lookup"><span data-stu-id="ac707-112">*IndexNumber*</span></span>  <br/> |<span data-ttu-id="ac707-113">Uma expressão de inteiro que representa um índice baseado em 1 para a lista dos itens depois dela.</span><span class="sxs-lookup"><span data-stu-id="ac707-113">An integer expression that represents a 1-based index into the list of the items following it.</span></span>  <br/> |
| <span data-ttu-id="ac707-114">*Valor*</span><span class="sxs-lookup"><span data-stu-id="ac707-114">*Value*</span></span>  <br/> |<span data-ttu-id="ac707-115">Lista de valores de qualquer tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ac707-115">List of values of any data type.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac707-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="ac707-116">Remarks</span></span>

<span data-ttu-id="ac707-117">Se o fornecido *Número_de_índice* não for um inteiro, o valor implicitamente é convertido em um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="ac707-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span></span> 
  
<span data-ttu-id="ac707-118">Se o valor de índice ultrapassar os limites da matriz de valores, **Escolher** retornará NULL.</span><span class="sxs-lookup"><span data-stu-id="ac707-118">If the index value exceeds the bounds of the array of values, **Choose** returns NULL.</span></span> 
  

