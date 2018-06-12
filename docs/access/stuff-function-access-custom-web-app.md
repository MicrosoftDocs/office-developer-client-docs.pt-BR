---
title: Função coisas (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Insere uma cadeia de caracteres de texto em outra cadeia de caracteres de texto. Ela exclui um tamanho especificado de caracteres na primeira cadeia de caracteres na posição inicial e, em seguida, insere a segunda cadeia a primeira cadeia de caracteres na posição inicial.
ms.openlocfilehash: 5540bb5936803370835a0c3d80b420edc13d0de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765232"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="ae1ee-104">Função coisas (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="ae1ee-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="ae1ee-105">Insere uma cadeia de caracteres de texto em outra cadeia de caracteres de texto.</span><span class="sxs-lookup"><span data-stu-id="ae1ee-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="ae1ee-106">Ela exclui um tamanho especificado de caracteres na primeira cadeia de caracteres na posição inicial e, em seguida, insere a segunda cadeia a primeira cadeia de caracteres na posição inicial.</span><span class="sxs-lookup"><span data-stu-id="ae1ee-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ae1ee-p103">[!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="ae1ee-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ae1ee-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae1ee-109">Syntax</span></span>

 <span data-ttu-id="ae1ee-110">**Coisas** (*IntoTextExpression*, *Iniciar*, *comprimento*, *ThisTextExpression*)</span><span class="sxs-lookup"><span data-stu-id="ae1ee-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="ae1ee-111">A função **coisas** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="ae1ee-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ae1ee-112">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="ae1ee-112">**Argument name**</span></span>|<span data-ttu-id="ae1ee-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ae1ee-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ae1ee-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="ae1ee-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="ae1ee-115">Uma expressão de texto que especifica o texto no qual o texto especificado pelo *ThisTextExpression* será inserido.</span><span class="sxs-lookup"><span data-stu-id="ae1ee-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="ae1ee-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="ae1ee-116">*Start*</span></span>  <br/> |<span data-ttu-id="ae1ee-117">Um valor integer que especifica o local para iniciar a inserção e exclusão.</span><span class="sxs-lookup"><span data-stu-id="ae1ee-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="ae1ee-118">Se o início ou o comprimento for negativo, uma cadeia de caracteres nula será retornada.</span><span class="sxs-lookup"><span data-stu-id="ae1ee-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="ae1ee-119">Se start for maior que o primeiro *IntoTextExpression* , uma cadeia de caracteres nula será retornada.</span><span class="sxs-lookup"><span data-stu-id="ae1ee-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="ae1ee-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="ae1ee-120">*Length*</span></span>  <br/> |<span data-ttu-id="ae1ee-121">Um inteiro que especifica o número de caracteres a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="ae1ee-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="ae1ee-122">Se length for maior que o primeiro *IntoTextExpression* , exclusão ocorre até o último caractere no último *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="ae1ee-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="ae1ee-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="ae1ee-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="ae1ee-124">Um texto chapéu de expressão Especifica o texto para inserir em *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="ae1ee-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="ae1ee-125">Esta expressão substituirá os caracteres de comprimento de início de *IntoTextExpression* em *Iniciar* .</span><span class="sxs-lookup"><span data-stu-id="ae1ee-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae1ee-126">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="ae1ee-126">Remarks</span></span>

<span data-ttu-id="ae1ee-127">Se os argumentos *Iniciar* ou *comprimento* são negativos, ou se a posição inicial for maior que o comprimento da cadeia de caracteres primeiro, uma cadeia de caracteres nula será retornada.</span><span class="sxs-lookup"><span data-stu-id="ae1ee-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="ae1ee-128">Se a posição inicial for 0, é retornado um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="ae1ee-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="ae1ee-129">Se o comprimento para excluir for maior que a primeira cadeia de caracteres, ele é excluído para o primeiro caractere na primeira cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ae1ee-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

