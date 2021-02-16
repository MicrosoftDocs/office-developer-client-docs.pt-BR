---
title: Função SubString (aplicativo da Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Retorna parte de uma expressão de texto.
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433469"
---
# <a name="substring-function-access-custom-web-app"></a><span data-ttu-id="400d4-103">Função SubString (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="400d4-103">SubString Function (Access custom web app)</span></span>

<span data-ttu-id="400d4-104">Retorna parte de uma expressão de texto.</span><span class="sxs-lookup"><span data-stu-id="400d4-104">Returns part of a text expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="400d4-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="400d4-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="400d4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="400d4-107">Syntax</span></span>

 <span data-ttu-id="400d4-108">**SubString** (*TextExpression*, *Start*, *Length*)</span><span class="sxs-lookup"><span data-stu-id="400d4-108">**SubString** (*TextExpression*, *Start*, *Length*)</span></span> 
  
<span data-ttu-id="400d4-109">A função **SubString** contém os argumentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="400d4-109">The **SubString** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="400d4-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="400d4-110">**Argument name**</span></span>|<span data-ttu-id="400d4-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="400d4-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="400d4-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="400d4-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="400d4-113">Uma expressão de texto.</span><span class="sxs-lookup"><span data-stu-id="400d4-113">A text expression.</span></span>  <br/> |
| <span data-ttu-id="400d4-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="400d4-114">*Start*</span></span>  <br/> |<span data-ttu-id="400d4-p102">Uma expressão de números inteiros que especifica o local no qual começam os caracteres retornados. Se essa expressão for menor que 1, a expressão retornada começará no primeiro caractere que é especificado na expressão. Nesse caso, o número de caracteres que são retornados é o maior valor da soma de início + o comprimento -1 ou 0. Se o início for maior que o número de caracteres na expressão de valor, uma expressão de comprimento zero será retornada.</span><span class="sxs-lookup"><span data-stu-id="400d4-p102">An integer expression that specifies where the returned characters start. If start is less than 1, the returned expression will begin at the first character that is specified in expression. In this case, the number of characters that are returned is the largest value of either the sum of start + length- 1 or 0. If start is greater than the number of characters in the value expression, a zero-length expression is returned.</span></span>  <br/> |
| <span data-ttu-id="400d4-119">*Length*</span><span class="sxs-lookup"><span data-stu-id="400d4-119">*Length*</span></span>  <br/> |<span data-ttu-id="400d4-p103">Uma expressão com um número inteiro positivo, que especifica quantos caracteres da expressão serão retornados. Se for negativo, é gerado um erro e a política é encerrada. Se a soma do início e a duração forem maiores que o número de caracteres na expressão, o início da expressão de valor inserida no início é retornado.</span><span class="sxs-lookup"><span data-stu-id="400d4-p103">A positive integer expression that specifies how many characters of the expression will be returned. If length is negative, an error is generated and the statement is terminated. If the sum of start and length is greater than the number of characters in expression, the whole value expression beginning at start is returned.</span></span>  <br/> |
   

