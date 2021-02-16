---
title: Bloco de dados ForEachRecord (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Um bloco de dados ForEachRecord repete um conjunto de instruções para cada registro em um domínio.
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428232"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a><span data-ttu-id="8a93b-103">Bloco de dados ForEachRecord (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="8a93b-103">ForEachRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="8a93b-104">Um **bloco de dados ForEachRecord** repete um conjunto de instruções para cada registro em um domínio.</span><span class="sxs-lookup"><span data-stu-id="8a93b-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8a93b-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="8a93b-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8a93b-107">O bloco de dados **ParaCadaRegistro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="8a93b-107">The **ForEachRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="8a93b-108">Setting</span><span class="sxs-lookup"><span data-stu-id="8a93b-108">Setting</span></span>

<span data-ttu-id="8a93b-109">A ação **ParaCadaRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="8a93b-109">The **ForEachRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="8a93b-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="8a93b-110">**Argument name**</span></span>|<span data-ttu-id="8a93b-111">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="8a93b-111">**Required**</span></span>|<span data-ttu-id="8a93b-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8a93b-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8a93b-113">**Em**</span><span class="sxs-lookup"><span data-stu-id="8a93b-113">**In**</span></span> <br/> |<span data-ttu-id="8a93b-114">Sim</span><span class="sxs-lookup"><span data-stu-id="8a93b-114">Yes</span></span>  <br/> |<span data-ttu-id="8a93b-115">Uma cadeia de caracteres que identifica o domínio de registros a ser utilizado.</span><span class="sxs-lookup"><span data-stu-id="8a93b-115">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="8a93b-116">O  *argumento In*  pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="8a93b-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> <span data-ttu-id="8a93b-117">**OBSERVAÇÃO:** o domínio especificado não pode incluir dados armazenados em uma tabela vinculada ou fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="8a93b-117">**NOTE**: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>           |
|<span data-ttu-id="8a93b-118">**Condição Where**</span><span class="sxs-lookup"><span data-stu-id="8a93b-118">**Where Condition**</span></span> <br/> |<span data-ttu-id="8a93b-119">Não</span><span class="sxs-lookup"><span data-stu-id="8a93b-119">No</span></span>  <br/> |<span data-ttu-id="8a93b-120">Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados **ForEachRecord** é executado.</span><span class="sxs-lookup"><span data-stu-id="8a93b-120">A string expression used to restrict the range of data on which the **ForEachRecord** data block is performed.</span></span> <span data-ttu-id="8a93b-121">Por exemplo, os critérios geralmente são equivalentes à cláusula WHERE em uma expressão SQL, sem a palavra WHERE.</span><span class="sxs-lookup"><span data-stu-id="8a93b-121">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="8a93b-122">Se os critérios são omitidos, o bloco de dados **ForEachRecord** opera em todo o domínio especificado pelo  *argumento*  In.</span><span class="sxs-lookup"><span data-stu-id="8a93b-122">If criteria are omitted, the **ForEachRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="8a93b-123">Qualquer campo incluído nos critérios também deve ser um campo em  *In*  .</span><span class="sxs-lookup"><span data-stu-id="8a93b-123">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
|<span data-ttu-id="8a93b-124">**Alias**</span><span class="sxs-lookup"><span data-stu-id="8a93b-124">**Alias**</span></span> <br/> |<span data-ttu-id="8a93b-125">Não</span><span class="sxs-lookup"><span data-stu-id="8a93b-125">No</span></span>  <br/> |<span data-ttu-id="8a93b-126">Uma cadeia de caracteres que fornece um nome alternativo para o domínio especificado pelo  *argumento*  In.</span><span class="sxs-lookup"><span data-stu-id="8a93b-126">A string that provides an alternative name for the domain specified by the  *In*  argument.</span></span> <span data-ttu-id="8a93b-127">Comumente usado para reduzir o nome da tabela para subsequentes referências, evitando referências ambíguas.</span><span class="sxs-lookup"><span data-stu-id="8a93b-127">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="8a93b-128">Se  *Alias*  não for especificado, o nome da tabela ou consulta será usado como o alias.</span><span class="sxs-lookup"><span data-stu-id="8a93b-128">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a93b-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a93b-129">Remarks</span></span>

<span data-ttu-id="8a93b-130">Use a ação **[SairparaCadaRegistro](exitforeachrecord-macro-action-access-custom-web-app.md)** para encerrar um bloco de dados **ParaCadaRegistro** imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8a93b-130">Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately.</span></span> 
  

