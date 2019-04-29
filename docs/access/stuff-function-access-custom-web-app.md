---
title: Função tudo (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Insere uma cadeia de caracteres de texto em outra sequência de texto. Ele exclui um tamanho especificado de caracteres na primeira cadeia de caracteres na posição inicial e insere a segunda cadeia de caracteres na primeira cadeia de caracteres na posição inicial.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427672"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="1473f-104">Função tudo (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="1473f-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="1473f-105">Insere uma cadeia de caracteres de texto em outra sequência de texto.</span><span class="sxs-lookup"><span data-stu-id="1473f-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="1473f-106">Ele exclui um tamanho especificado de caracteres na primeira cadeia de caracteres na posição inicial e insere a segunda cadeia de caracteres na primeira cadeia de caracteres na posição inicial.</span><span class="sxs-lookup"><span data-stu-id="1473f-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="1473f-p103">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="1473f-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1473f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1473f-109">Syntax</span></span>

 <span data-ttu-id="1473f-110">**Coisas** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span><span class="sxs-lookup"><span data-stu-id="1473f-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="1473f-111">A função **tudo** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="1473f-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="1473f-112">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="1473f-112">**Argument name**</span></span>|<span data-ttu-id="1473f-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1473f-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1473f-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="1473f-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="1473f-115">Uma expressão de texto que especifica o texto no qual o texto especificado pelo *ThisTextExpression* será inserido.</span><span class="sxs-lookup"><span data-stu-id="1473f-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="1473f-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="1473f-116">*Start*</span></span>  <br/> |<span data-ttu-id="1473f-117">Um valor inteiro que especifica o local para iniciar a exclusão e a inserção.</span><span class="sxs-lookup"><span data-stu-id="1473f-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="1473f-118">Se Start ou length for negativo, uma cadeia de caracteres nula será retornada.</span><span class="sxs-lookup"><span data-stu-id="1473f-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="1473f-119">Se Start for maior que o primeiro *IntoTextExpression* , uma cadeia de caracteres nula será retornada.</span><span class="sxs-lookup"><span data-stu-id="1473f-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="1473f-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="1473f-120">*Length*</span></span>  <br/> |<span data-ttu-id="1473f-121">Um inteiro que especifica o número de caracteres a serem excluídos.</span><span class="sxs-lookup"><span data-stu-id="1473f-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="1473f-122">Se length for maior que o primeiro *IntoTextExpression* , a exclusão ocorrerá até o último caractere no último *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="1473f-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="1473f-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="1473f-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="1473f-124">Uma expressão de texto Hat especifica o texto a ser inserido no *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="1473f-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="1473f-125">Essa expressão substituirá os caracteres de comprimento de *IntoTextExpression* começando no *início* .</span><span class="sxs-lookup"><span data-stu-id="1473f-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1473f-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1473f-126">Remarks</span></span>

<span data-ttu-id="1473f-127">Se os argumentos *Start* ou *Length* forem negativos, ou se a posição inicial for maior do que o comprimento da primeira cadeia de caracteres, uma cadeia de caracteres nula será retornada.</span><span class="sxs-lookup"><span data-stu-id="1473f-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="1473f-128">Se a posição inicial for 0, um valor nulo será retornado.</span><span class="sxs-lookup"><span data-stu-id="1473f-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="1473f-129">Se o comprimento a ser excluído for maior que a primeira cadeia de caracteres, ele será excluído para o primeiro caractere na primeira cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1473f-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

