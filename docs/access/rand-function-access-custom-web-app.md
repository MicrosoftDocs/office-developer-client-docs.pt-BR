---
title: Função RAND (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: Retorna um número pseudo-aleatório entre 0 e 1.
ms.openlocfilehash: ed0f9991b2b1d9553d6d45524d6b1e4e5321ea7e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765210"
---
# <a name="rand-function-access-custom-web-app"></a><span data-ttu-id="16941-103">Função RAND (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="16941-103">Rand Function (Access custom web app)</span></span>

<span data-ttu-id="16941-104">Retorna um número pseudo-aleatório entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="16941-104">Returns a pseudo-random number between 0 and 1.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="16941-p101">[!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="16941-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="16941-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="16941-107">Syntax</span></span>

 <span data-ttu-id="16941-108">**Rand** ([ *Propagação* ])</span><span class="sxs-lookup"><span data-stu-id="16941-108">**Rand** ( [  *Seed*  ])</span></span> 
  
<span data-ttu-id="16941-109">A função **Rand** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="16941-109">The **Rand** function contains the following argument.</span></span> 
  
|<span data-ttu-id="16941-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="16941-110">**Argument name**</span></span>|<span data-ttu-id="16941-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="16941-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="16941-112">*Seed*</span><span class="sxs-lookup"><span data-stu-id="16941-112">*Seed*</span></span>  <br/> |<span data-ttu-id="16941-113">Uma expressão de inteiro que retornará o valor de propagação.</span><span class="sxs-lookup"><span data-stu-id="16941-113">An integer expression that gives the seed value.</span></span> <span data-ttu-id="16941-114">Se *propagar* não for especificado, um valor de propagação é atribuído aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="16941-114">If  *Seed*  is not specified, a seed value is assigned at random.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16941-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="16941-115">Remarks</span></span>

<span data-ttu-id="16941-116">Chamadas repetitivas da função **Rand** com a mesma propagação retornam os mesmos resultados.</span><span class="sxs-lookup"><span data-stu-id="16941-116">Repetitive calls of the **Rand** function with the same seed return the same results.</span></span> 
  

