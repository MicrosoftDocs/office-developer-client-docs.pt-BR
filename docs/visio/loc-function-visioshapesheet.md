---
title: Função LOC (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Usa um ponto definido nas coordenadas locais de uma forma e retorna o ponto equivalente expresso nas coordenadas locais da forma associada à fórmula.
ms.openlocfilehash: 4728e5f8301c6ef10ddb0c14b6c0868a7a48b2a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422422"
---
# <a name="loc-function-visioshapesheet"></a><span data-ttu-id="721f0-103">Função LOC (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="721f0-103">LOC Function (VisioShapeSheet)</span></span>

<span data-ttu-id="721f0-104">Usa um ponto definido nas coordenadas locais de uma forma e retorna o ponto equivalente expresso nas coordenadas locais da forma associada à fórmula.</span><span class="sxs-lookup"><span data-stu-id="721f0-104">Takes a point defined in one shape's local coordinates and returns the equivalent point expressed in the local coordinates of the shape associated with the formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="721f0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="721f0-105">Syntax</span></span>

<span data-ttu-id="721f0-106">LOC (\* \* *ponto* \* \*)</span><span class="sxs-lookup"><span data-stu-id="721f0-106">LOC(\*\* *point* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="721f0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="721f0-107">Parameters</span></span>

|<span data-ttu-id="721f0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="721f0-108">**Name**</span></span>|<span data-ttu-id="721f0-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="721f0-109">**Required/Optional**</span></span>|<span data-ttu-id="721f0-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="721f0-110">**Data Type**</span></span>|<span data-ttu-id="721f0-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="721f0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="721f0-112">_ponto_</span><span class="sxs-lookup"><span data-stu-id="721f0-112">_point_</span></span> <br/> |<span data-ttu-id="721f0-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="721f0-113">Required</span></span>  <br/> |<span data-ttu-id="721f0-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="721f0-114">**String**</span></span> <br/> | <span data-ttu-id="721f0-115">Um ponto definido nas coordenadas locais de uma forma.</span><span class="sxs-lookup"><span data-stu-id="721f0-115">A point defined in one shape's local coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="721f0-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="721f0-116">Return value</span></span>

<span data-ttu-id="721f0-117">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="721f0-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="721f0-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="721f0-118">Remarks</span></span>

<span data-ttu-id="721f0-p101">As coordenadas locais são medidas do canto inferior esquerdo do retângulo de seleção da forma. Ambas as formas devem estar na mesma página.</span><span class="sxs-lookup"><span data-stu-id="721f0-p101">Local coordinates are measured from the lower-left corner of the shape's selection rectangle. Both shapes must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="721f0-121">Exemplo</span><span class="sxs-lookup"><span data-stu-id="721f0-121">Example</span></span>

<span data-ttu-id="721f0-122">LOC (PNT (Sheet. 5! LocPinX, sheet. 5! LocPinY))</span><span class="sxs-lookup"><span data-stu-id="721f0-122">LOC(PNT(Sheet.5!LocPinX, Sheet.5!LocPinY))</span></span> 
  
<span data-ttu-id="721f0-p102">Nesta expressão, PNT converte um conjunto de coordenadas locais em Sheet.5 para um ponto. (Sheet.5 é uma outra forma na mesma página de desenho.) Em seguida, LOC converte esse ponto para um ponto equivalente no sistema de coordenadas locais da forma atual, em relação ao canto inferior esquerdo do retângulo de seleção da forma atual.</span><span class="sxs-lookup"><span data-stu-id="721f0-p102">In this expression, PNT converts a set of local coordinates in Sheet.5 to a point. (Sheet.5 is another shape on the same drawing page.) LOC then converts that point to an equivalent point in the current shape's local coordinate system, relative to the lower-left corner of the selection rectangle of the current shape.</span></span> 
  
<span data-ttu-id="721f0-125">O 5 em Sheet.5 é o número de identificação da forma, exibido na caixa de diálogo **Nome da Forma** (guia **Desenvolvedor**).</span><span class="sxs-lookup"><span data-stu-id="721f0-125">The 5 in Sheet.5 is the ID number for the shape, which is displayed in the **Shape Name** dialog box (**Developer** tab).</span></span> 
  

