---
title: Bloco de dados Pesquisarregistro (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Um bloco de dados PesquisarRegistro executa um conjunto de ações em um registro específico.
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434358"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="fafcb-103">Bloco de dados Pesquisarregistro (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="fafcb-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="fafcb-104">Um bloco de dados **PesquisarRegistro** executa um conjunto de ações em um registro específico.</span><span class="sxs-lookup"><span data-stu-id="fafcb-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="fafcb-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="fafcb-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fafcb-107">O bloco de dados **PesquisarRegistro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="fafcb-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="fafcb-108">Setting</span><span class="sxs-lookup"><span data-stu-id="fafcb-108">Setting</span></span>

<span data-ttu-id="fafcb-109">A ação **PesquisarRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="fafcb-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="fafcb-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="fafcb-110">**Argument**</span></span>|<span data-ttu-id="fafcb-111">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="fafcb-111">**Required**</span></span>|<span data-ttu-id="fafcb-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fafcb-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="fafcb-113">_No_</span><span class="sxs-lookup"><span data-stu-id="fafcb-113">_In_</span></span> <br/> |<span data-ttu-id="fafcb-114">Sim</span><span class="sxs-lookup"><span data-stu-id="fafcb-114">Yes</span></span>  <br/> |<span data-ttu-id="fafcb-115">Uma cadeia de caracteres que identifica o registro a ser utilizado.</span><span class="sxs-lookup"><span data-stu-id="fafcb-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="fafcb-116">O argumento *in* pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="fafcb-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="fafcb-117">_Condição Where_</span><span class="sxs-lookup"><span data-stu-id="fafcb-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="fafcb-118">Não</span><span class="sxs-lookup"><span data-stu-id="fafcb-118">No</span></span>  <br/> |<span data-ttu-id="fafcb-119">Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados **PesquisarRegistro** opera.</span><span class="sxs-lookup"><span data-stu-id="fafcb-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="fafcb-120">Por exemplo, os critérios geralmente são equivalentes à cláusula WHERE em uma expressão SQL, sem a palavra WHERE.</span><span class="sxs-lookup"><span data-stu-id="fafcb-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="fafcb-121">Se criteria for omitido, o bloco de dados **pesquisarregistro** funcionará em todo o domínio especificado pelo argumento *in* .</span><span class="sxs-lookup"><span data-stu-id="fafcb-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="fafcb-122">Qualquer campo incluído nos critérios também deve ser um campo no *no* .</span><span class="sxs-lookup"><span data-stu-id="fafcb-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="fafcb-123">_Alias_</span><span class="sxs-lookup"><span data-stu-id="fafcb-123">_Alias_</span></span> <br/> |<span data-ttu-id="fafcb-124">Não</span><span class="sxs-lookup"><span data-stu-id="fafcb-124">No</span></span>  <br/> |<span data-ttu-id="fafcb-125">Uma cadeia de caracteres que fornece um nome alternativo para o registro especificado pelo argumento *in* .</span><span class="sxs-lookup"><span data-stu-id="fafcb-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="fafcb-126">Comumente usado para reduzir o nome da tabela para subsequentes referências, evitando referências ambíguas.</span><span class="sxs-lookup"><span data-stu-id="fafcb-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="fafcb-127">Se *alias* não for especificado, o nome da tabela ou da consulta será usado como o alias.</span><span class="sxs-lookup"><span data-stu-id="fafcb-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fafcb-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="fafcb-128">Remarks</span></span>

<span data-ttu-id="fafcb-129">Se o critério especificado pelos argumentos  *Em*  e  *Condição Where*  especificar mais de um registro, o bloco de dados **PesquisarRegistro** será executado somente no primeiro registro.</span><span class="sxs-lookup"><span data-stu-id="fafcb-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="fafcb-130">Se nenhum registro satisfizer *em que condição* ou se *in* não contiver registros, **pesquisarregistro** cria um registro em branco no qual todos os campos contêm um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="fafcb-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

