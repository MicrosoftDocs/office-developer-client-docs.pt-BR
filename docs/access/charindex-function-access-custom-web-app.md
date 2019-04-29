---
title: Função CharIndex (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Pesquisa uma expressão de texto para outra expressão de texto e retorna sua posição inicial, se encontrada.
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423129"
---
# <a name="charindex-function-access-custom-web-app"></a><span data-ttu-id="11aa2-103">Função CharIndex (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="11aa2-103">CharIndex function (Access custom web app)</span></span>

<span data-ttu-id="11aa2-104">Pesquisa uma expressão de texto para outra expressão de texto e retorna sua posição inicial, se encontrada.</span><span class="sxs-lookup"><span data-stu-id="11aa2-104">Searches a text expression for another text expression and returns its starting position if found.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="11aa2-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="11aa2-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="11aa2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11aa2-107">Syntax</span></span>

<span data-ttu-id="11aa2-108">**CharIndex** (*TextName*, *WithinText*, [*Start*])</span><span class="sxs-lookup"><span data-stu-id="11aa2-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span></span> 
  
|<span data-ttu-id="11aa2-109">**Nome do Argumento**</span><span class="sxs-lookup"><span data-stu-id="11aa2-109">**Argument Name**</span></span>|<span data-ttu-id="11aa2-110">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="11aa2-110">**Required**</span></span>|<span data-ttu-id="11aa2-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="11aa2-111">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="11aa2-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="11aa2-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="11aa2-113">Sim</span><span class="sxs-lookup"><span data-stu-id="11aa2-113">Yes</span></span>  <br/> |<span data-ttu-id="11aa2-114">Uma expressão de texto que contém o texto a ser localizado.</span><span class="sxs-lookup"><span data-stu-id="11aa2-114">A text expression that contains the text to be found.</span></span>  <br/> |
| <span data-ttu-id="11aa2-115">*WithinText*</span><span class="sxs-lookup"><span data-stu-id="11aa2-115">*WithinText*</span></span>  <br/> |<span data-ttu-id="11aa2-116">Sim</span><span class="sxs-lookup"><span data-stu-id="11aa2-116">Yes</span></span>  <br/> |<span data-ttu-id="11aa2-117">A expressão de texto a ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="11aa2-117">The text expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="11aa2-118">*Start*</span><span class="sxs-lookup"><span data-stu-id="11aa2-118">*Start*</span></span>  <br/> |<span data-ttu-id="11aa2-119">Não</span><span class="sxs-lookup"><span data-stu-id="11aa2-119">No</span></span>  <br/> |<span data-ttu-id="11aa2-120">Um inteiro que especifica o local no *WithinText* para iniciar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="11aa2-120">An integer that specifies the location in  *WithinText*  to begin the search.</span></span> <span data-ttu-id="11aa2-121">Se *Start* não for especificado, for um número negativo ou for 0, a pesquisa começará no início de *WithinText* .</span><span class="sxs-lookup"><span data-stu-id="11aa2-121">If  *Start*  is not specified, is a negative number, or is 0, the search starts at the beginning of  *WithinText*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11aa2-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="11aa2-122">Remarks</span></span>

<span data-ttu-id="11aa2-123">Se *textName* ou *WithinText* for NULL, *charIndex* retornará NULL.</span><span class="sxs-lookup"><span data-stu-id="11aa2-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span></span> 
  
<span data-ttu-id="11aa2-124">Se *textName* não for encontrado dentro de *WithinText*, *charIndex* retornará 0.</span><span class="sxs-lookup"><span data-stu-id="11aa2-124">If  *TextExpression*  is not found within  *WithinText*,  *CharIndex*  returns 0.</span></span> 
  
<span data-ttu-id="11aa2-125">A posição inicial retornada é baseada em 1, não em 0.</span><span class="sxs-lookup"><span data-stu-id="11aa2-125">The starting position returned is 1-based, not 0-based.</span></span>
  

