---
title: Função CharIndex (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Pesquisas uma expressão de texto para outra expressão de texto e retorna suas Iniciando posição se encontrado.
ms.openlocfilehash: 86a46f57c64028530217326127eece887127c4c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765083"
---
# <a name="charindex-function-access-custom-web-app"></a><span data-ttu-id="3fa2a-103">Função CharIndex (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="3fa2a-103">CharIndex function (Access custom web app)</span></span>

<span data-ttu-id="3fa2a-104">Pesquisas uma expressão de texto para outra expressão de texto e retorna suas Iniciando posição se encontrado.</span><span class="sxs-lookup"><span data-stu-id="3fa2a-104">Searches a text expression for another text expression and returns its starting position if found.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3fa2a-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="3fa2a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3fa2a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fa2a-107">Syntax</span></span>

<span data-ttu-id="3fa2a-108">**CharIndex** (*TextExpression*, *WithinText*, [*Iniciar*])</span><span class="sxs-lookup"><span data-stu-id="3fa2a-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span></span> 
  
|<span data-ttu-id="3fa2a-109">**Nome do Argumento**</span><span class="sxs-lookup"><span data-stu-id="3fa2a-109">**Argument Name**</span></span>|<span data-ttu-id="3fa2a-110">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="3fa2a-110">**Required**</span></span>|<span data-ttu-id="3fa2a-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3fa2a-111">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="3fa2a-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="3fa2a-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="3fa2a-113">Sim</span><span class="sxs-lookup"><span data-stu-id="3fa2a-113">Yes</span></span>  <br/> |<span data-ttu-id="3fa2a-114">Uma expressão de texto que contém o texto a ser localizado.</span><span class="sxs-lookup"><span data-stu-id="3fa2a-114">A text expression that contains the text to be found.</span></span>  <br/> |
| <span data-ttu-id="3fa2a-115">*WithinText*</span><span class="sxs-lookup"><span data-stu-id="3fa2a-115">*WithinText*</span></span>  <br/> |<span data-ttu-id="3fa2a-116">Sim</span><span class="sxs-lookup"><span data-stu-id="3fa2a-116">Yes</span></span>  <br/> |<span data-ttu-id="3fa2a-117">A expressão de texto a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="3fa2a-117">The text expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="3fa2a-118">*Start*</span><span class="sxs-lookup"><span data-stu-id="3fa2a-118">*Start*</span></span>  <br/> |<span data-ttu-id="3fa2a-119">Não</span><span class="sxs-lookup"><span data-stu-id="3fa2a-119">No</span></span>  <br/> |<span data-ttu-id="3fa2a-120">Um inteiro que especifica o local em *WithinText* para iniciar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="3fa2a-120">An integer that specifies the location in  *WithinText*  to begin the search.</span></span> <span data-ttu-id="3fa2a-121">Se *Iniciar* não for especificado, for um número negativo ou for 0, a pesquisa começa no início do *WithinText* .</span><span class="sxs-lookup"><span data-stu-id="3fa2a-121">If  *Start*  is not specified, is a negative number, or is 0, the search starts at the beginning of  *WithinText*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fa2a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fa2a-122">Remarks</span></span>

<span data-ttu-id="3fa2a-123">Se *TextExpression* ou *WithinText* for NULL, *CharIndex* retornará NULL.</span><span class="sxs-lookup"><span data-stu-id="3fa2a-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span></span> 
  
<span data-ttu-id="3fa2a-124">Se *TextExpression* não for encontrado na *WithinText*, *CharIndex* retornará 0.</span><span class="sxs-lookup"><span data-stu-id="3fa2a-124">If  *TextExpression*  is not found within  *WithinText*,  *CharIndex*  returns 0.</span></span> 
  
<span data-ttu-id="3fa2a-125">A posição inicial retornada é baseado em 1, não baseado em 0.</span><span class="sxs-lookup"><span data-stu-id="3fa2a-125">The starting position returned is 1-based, not 0-based.</span></span>
  

