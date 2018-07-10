---
title: Função CONCATENAR (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Retorna uma cadeia de caracteres com o resultado da combinação de dois ou mais valores de cadeia de caracteres.
ms.openlocfilehash: fc0de43e5e42cc1c39ee89cf76058b8039daf279
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765040"
---
# <a name="concat-function-access-custom-web-app"></a><span data-ttu-id="281b8-103">Função CONCATENAR (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="281b8-103">Concat function (Access custom web app)</span></span>

<span data-ttu-id="281b8-104">Retorna uma cadeia de caracteres com o resultado da combinação de dois ou mais valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="281b8-104">Returns a string that is the result of combining two or more string values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="281b8-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="281b8-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="281b8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="281b8-107">Syntax</span></span>

<span data-ttu-id="281b8-108">**Concat** (*Value1*, *Value2*,... [*ValueN*])</span><span class="sxs-lookup"><span data-stu-id="281b8-108">**Concat** (*Value1*, *Value2*, …[*ValueN*])</span></span> 
  
<span data-ttu-id="281b8-109">A função **Concat** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="281b8-109">The **Concat** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="281b8-110">**Nome do Argumento**</span><span class="sxs-lookup"><span data-stu-id="281b8-110">**Argument Name**</span></span>|<span data-ttu-id="281b8-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="281b8-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="281b8-112">Value</span><span class="sxs-lookup"><span data-stu-id="281b8-112">Value</span></span>  <br/> |<span data-ttu-id="281b8-113">Um valor de cadeia de caracteres a ser concatenado para outros valores.</span><span class="sxs-lookup"><span data-stu-id="281b8-113">A string value to concatenate to the other values.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="281b8-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="281b8-114">Remarks</span></span>

<span data-ttu-id="281b8-p102">A função **Concat** concatena um número de variável de argumento de cadeia de caracteres em uma única cadeia de caracteres. É necessário haver um mínimo de dois argumentos de cadeia de caracteres, do contrário ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="281b8-p102">**Concat** takes a variable number of string arguments and concatenates them into a single string. A minimum of two string arguments are required; otherwise, an error is raised.</span></span> 
  
<span data-ttu-id="281b8-117">Todos os argumentos são implicitamente convertidos em tipos de dados de cadeia de caracteres e, em seguida, concatenados.</span><span class="sxs-lookup"><span data-stu-id="281b8-117">All arguments are implicitly converted to string data types and then concatenated.</span></span>
  
## <a name="example"></a><span data-ttu-id="281b8-118">Example</span><span class="sxs-lookup"><span data-stu-id="281b8-118">Example</span></span>

<span data-ttu-id="281b8-119">A expressão a seguir pode ser usada para exibir o nome completo de uma pessoa em um dos campos da tabela Nome, Sobrenome e Nome do Meio.</span><span class="sxs-lookup"><span data-stu-id="281b8-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="281b8-120">Se o campo MiddleInitial estiver vazio, somente os campos FirstName e LastName são combinados para exibir o nome completo.</span><span class="sxs-lookup"><span data-stu-id="281b8-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


