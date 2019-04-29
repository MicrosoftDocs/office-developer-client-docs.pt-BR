---
title: Função Rand (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: Retorna um número pseudo aleatório entre 0 e 1.
ms.openlocfilehash: 02d914de9d74083a6ebf76f6d0e556fe51954a24
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416605"
---
# <a name="rand-function-access-custom-web-app"></a><span data-ttu-id="ff1d0-103">Função Rand (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="ff1d0-103">Rand Function (Access custom web app)</span></span>

<span data-ttu-id="ff1d0-104">Retorna um número pseudo aleatório entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="ff1d0-104">Returns a pseudo-random number between 0 and 1.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ff1d0-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="ff1d0-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ff1d0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff1d0-107">Syntax</span></span>

 <span data-ttu-id="ff1d0-108">**Rand** ([ *Semente* ])</span><span class="sxs-lookup"><span data-stu-id="ff1d0-108">**Rand** ( [  *Seed*  ])</span></span> 
  
<span data-ttu-id="ff1d0-109">A função **Rand** contém o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff1d0-109">The **Rand** function contains the following argument.</span></span> 
  
|<span data-ttu-id="ff1d0-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="ff1d0-110">**Argument name**</span></span>|<span data-ttu-id="ff1d0-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ff1d0-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ff1d0-112">*Seed*</span><span class="sxs-lookup"><span data-stu-id="ff1d0-112">*Seed*</span></span>  <br/> |<span data-ttu-id="ff1d0-113">Uma expressão de inteiro que retorna o valor semente.</span><span class="sxs-lookup"><span data-stu-id="ff1d0-113">An integer expression that gives the seed value.</span></span> <span data-ttu-id="ff1d0-114">Se *propagação* não for especificada, um valor de semente será atribuído aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="ff1d0-114">If  *Seed*  is not specified, a seed value is assigned at random.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff1d0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff1d0-115">Remarks</span></span>

<span data-ttu-id="ff1d0-116">As chamadas repetitivas da função **Rand** com a mesma semente retornam os mesmos resultados.</span><span class="sxs-lookup"><span data-stu-id="ff1d0-116">Repetitive calls of the **Rand** function with the same seed return the same results.</span></span> 
  

