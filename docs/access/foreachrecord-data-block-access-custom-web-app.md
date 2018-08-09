---
title: Bloco de dados ParaCadaRegistro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Um bloco de dados ParaCadaRegistro repete um conjunto de instruções para cada registro em um domínio.
ms.openlocfilehash: 8ad14a01be05de9fb34299e49a9737f2009ef5ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765082"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a><span data-ttu-id="afc60-103">Bloco de dados ParaCadaRegistro (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="afc60-103">ForEachRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="afc60-104">Um bloco de dados **ParaCadaRegistro** repete um conjunto de instruções para cada registro em um domínio.</span><span class="sxs-lookup"><span data-stu-id="afc60-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="afc60-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="afc60-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="afc60-107">[!OBSERVAçãO] O bloco de dados **ParaCadaRegistro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="afc60-107">The **ForEachRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="afc60-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="afc60-108">Setting</span></span>

<span data-ttu-id="afc60-109">A ação **ParaCadaRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="afc60-109">The **ForEachRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="afc60-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="afc60-110">**Argument name**</span></span>|<span data-ttu-id="afc60-111">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="afc60-111">**Required**</span></span>|<span data-ttu-id="afc60-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="afc60-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="afc60-113">**Em**</span><span class="sxs-lookup"><span data-stu-id="afc60-113">**In**</span></span> <br/> |<span data-ttu-id="afc60-114">Sim</span><span class="sxs-lookup"><span data-stu-id="afc60-114">Yes</span></span>  <br/> |<span data-ttu-id="afc60-115">Uma cadeia de caracteres que identifica o domínio de registros para operar em.</span><span class="sxs-lookup"><span data-stu-id="afc60-115">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="afc60-116">O argumento *em* pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="afc60-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> <span data-ttu-id="afc60-117">**Observação**: O domínio especificado não pode incluir dados armazenados em uma tabela vinculada ou fonte de dados ODBC.</span><span class="sxs-lookup"><span data-stu-id="afc60-117">**NOTE**: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>           |
|<span data-ttu-id="afc60-118">**Condição Where**</span><span class="sxs-lookup"><span data-stu-id="afc60-118">**Where Condition**</span></span> <br/> |<span data-ttu-id="afc60-119">Não</span><span class="sxs-lookup"><span data-stu-id="afc60-119">No</span></span>  <br/> |<span data-ttu-id="afc60-120">Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados **ParaCadaRegistro** é executada.</span><span class="sxs-lookup"><span data-stu-id="afc60-120">A string expression used to restrict the range of data on which the **ForEachRecord** data block is performed.</span></span> <span data-ttu-id="afc60-121">Por exemplo, critérios costuma ser equivalente à cláusula WHERE em uma expressão SQL, sem a palavra onde.</span><span class="sxs-lookup"><span data-stu-id="afc60-121">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="afc60-122">Se os critérios forem omitidos, o bloco de dados **ParaCadaRegistro** opera em todo o domínio especificado pelo argumento *em* .</span><span class="sxs-lookup"><span data-stu-id="afc60-122">If criteria are omitted, the **ForEachRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="afc60-123">Qualquer campo que está incluído nos critérios também deve ser um campo no *In* .</span><span class="sxs-lookup"><span data-stu-id="afc60-123">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
|<span data-ttu-id="afc60-124">**Alias**</span><span class="sxs-lookup"><span data-stu-id="afc60-124">**Alias**</span></span> <br/> |<span data-ttu-id="afc60-125">Não</span><span class="sxs-lookup"><span data-stu-id="afc60-125">No</span></span>  <br/> |<span data-ttu-id="afc60-126">Uma cadeia de caracteres que fornece um nome alternativo para o domínio especificado pelo argumento *em* .</span><span class="sxs-lookup"><span data-stu-id="afc60-126">A string that provides an alternative name for the domain specified by the  *In*  argument.</span></span> <span data-ttu-id="afc60-127">Frequentemente usado para reduzir o nome da tabela referências posteriores evitar possíveis referências ambíguas.</span><span class="sxs-lookup"><span data-stu-id="afc60-127">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="afc60-128">Se o *Alias* não for especificado, o nome da tabela ou consulta será usado como o alias.</span><span class="sxs-lookup"><span data-stu-id="afc60-128">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="afc60-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="afc60-129">Remarks</span></span>

<span data-ttu-id="afc60-130">Use a ação **[SairparaCadaRegistro](exitforeachrecord-macro-action-access-custom-web-app.md)** para encerrar um bloco de dados **ParaCadaRegistro** imediatamente.</span><span class="sxs-lookup"><span data-stu-id="afc60-130">Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately.</span></span> 
  

