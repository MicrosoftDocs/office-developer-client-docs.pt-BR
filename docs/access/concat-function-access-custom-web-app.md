---
title: Função Concat (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Retorna uma cadeia de caracteres com o resultado da combinação de dois ou mais valores de cadeia de caracteres.
ms.openlocfilehash: b8f52c292e64939f9464bc666ecc4bc341580f94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423269"
---
# <a name="concat-function-access-custom-web-app"></a><span data-ttu-id="549d2-103">Função Concat (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="549d2-103">Concat function (Access custom web app)</span></span>

<span data-ttu-id="549d2-104">Retorna uma cadeia de caracteres com o resultado da combinação de dois ou mais valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="549d2-104">Returns a string that is the result of combining two or more string values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="549d2-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="549d2-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="549d2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="549d2-107">Syntax</span></span>

<span data-ttu-id="549d2-108">**Concat** (*Valor1*, *Valor2*, …[*ValorN*])</span><span class="sxs-lookup"><span data-stu-id="549d2-108">**Concat** (*Value1*, *Value2*, …[*ValueN*])</span></span> 
  
<span data-ttu-id="549d2-109">A função **Concat** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="549d2-109">The **Concat** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="549d2-110">**Nome do Argumento**</span><span class="sxs-lookup"><span data-stu-id="549d2-110">**Argument Name**</span></span>|<span data-ttu-id="549d2-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="549d2-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="549d2-112">Valor</span><span class="sxs-lookup"><span data-stu-id="549d2-112">Value</span></span>  <br/> |<span data-ttu-id="549d2-113">Um valor de cadeia de caracteres a ser concatenado para outros valores.</span><span class="sxs-lookup"><span data-stu-id="549d2-113">A string value to concatenate to the other values.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="549d2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="549d2-114">Remarks</span></span>

<span data-ttu-id="549d2-p102">A função **Concat** concatena um número de variável de argumento de cadeia de caracteres em uma única cadeia de caracteres. É necessário haver um mínimo de dois argumentos de cadeia de caracteres, do contrário ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="549d2-p102">**Concat** takes a variable number of string arguments and concatenates them into a single string. A minimum of two string arguments are required; otherwise, an error is raised.</span></span> 
  
<span data-ttu-id="549d2-117">Todos os argumentos são implicitamente convertidos em tipos de dados de cadeia de caracteres e, em seguida, concatenados.</span><span class="sxs-lookup"><span data-stu-id="549d2-117">All arguments are implicitly converted to string data types and then concatenated.</span></span>
  
## <a name="example"></a><span data-ttu-id="549d2-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="549d2-118">Example</span></span>

<span data-ttu-id="549d2-119">A expressão a seguir pode ser usada para exibir o nome completo de uma pessoa quando a tabela contém os campos Nome, Nome do Meio e Sobrenome.</span><span class="sxs-lookup"><span data-stu-id="549d2-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="549d2-120">Se o campo Nome do Meio estiver em branco, apenas os campos de Nome e Sobrenome serão combinados para exibir o nome completo.</span><span class="sxs-lookup"><span data-stu-id="549d2-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


