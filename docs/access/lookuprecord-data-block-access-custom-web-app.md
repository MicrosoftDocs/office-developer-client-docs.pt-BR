---
title: Bloco de dados Pesquisarregistro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Um bloco de dados PesquisarRegistro executa um conjunto de ações em um registro específico.
ms.openlocfilehash: 7012fecdf0e73647b2b8177473dd8b5540b5fcca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765106"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="526a7-103">Bloco de dados Pesquisarregistro (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="526a7-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="526a7-104">Um bloco de dados **PesquisarRegistro** executa um conjunto de ações em um registro específico.</span><span class="sxs-lookup"><span data-stu-id="526a7-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="526a7-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="526a7-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="526a7-107">[!OBSERVAçãO] O bloco de dados **PesquisarRegistro** está disponível somente em Macros de Dados.</span><span class="sxs-lookup"><span data-stu-id="526a7-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="526a7-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="526a7-108">Setting</span></span>

<span data-ttu-id="526a7-109">A ação **PesquisarRegistro** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="526a7-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="526a7-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="526a7-110">**Argument**</span></span>|<span data-ttu-id="526a7-111">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="526a7-111">**Required**</span></span>|<span data-ttu-id="526a7-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="526a7-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="526a7-113">_Em_</span><span class="sxs-lookup"><span data-stu-id="526a7-113">_In_</span></span> <br/> |<span data-ttu-id="526a7-114">Sim</span><span class="sxs-lookup"><span data-stu-id="526a7-114">Yes</span></span>  <br/> |<span data-ttu-id="526a7-115">Uma cadeia de caracteres que identifica o registro para operar em.</span><span class="sxs-lookup"><span data-stu-id="526a7-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="526a7-116">O argumento *em* pode conter o nome da tabela, uma consulta seleção ou uma instrução SQL.</span><span class="sxs-lookup"><span data-stu-id="526a7-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="526a7-117">_Condição Where_</span><span class="sxs-lookup"><span data-stu-id="526a7-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="526a7-118">Não</span><span class="sxs-lookup"><span data-stu-id="526a7-118">No</span></span>  <br/> |<span data-ttu-id="526a7-119">Uma expressão de cadeia de caracteres usada para restringir o intervalo de dados no qual o bloco de dados **Pesquisarregistro** é executada.</span><span class="sxs-lookup"><span data-stu-id="526a7-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="526a7-120">Por exemplo, critérios costuma ser equivalente à cláusula WHERE em uma expressão SQL, sem a palavra onde.</span><span class="sxs-lookup"><span data-stu-id="526a7-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="526a7-121">Se os critérios for omitido, o bloco de dados **Pesquisarregistro** opera em todo o domínio especificado pelo argumento *em* .</span><span class="sxs-lookup"><span data-stu-id="526a7-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="526a7-122">Qualquer campo que está incluído nos critérios também deve ser um campo no *In* .</span><span class="sxs-lookup"><span data-stu-id="526a7-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="526a7-123">_Alias_</span><span class="sxs-lookup"><span data-stu-id="526a7-123">_Alias_</span></span> <br/> |<span data-ttu-id="526a7-124">Não</span><span class="sxs-lookup"><span data-stu-id="526a7-124">No</span></span>  <br/> |<span data-ttu-id="526a7-125">Uma cadeia de caracteres que fornece um nome alternativo para o registro especificado pelo argumento *em* .</span><span class="sxs-lookup"><span data-stu-id="526a7-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="526a7-126">Frequentemente usado para reduzir o nome da tabela referências posteriores evitar possíveis referências ambíguas.</span><span class="sxs-lookup"><span data-stu-id="526a7-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="526a7-127">Se o *Alias* não for especificado, o nome da tabela ou consulta será usado como o alias.</span><span class="sxs-lookup"><span data-stu-id="526a7-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="526a7-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="526a7-128">Remarks</span></span>

<span data-ttu-id="526a7-129">Se o critério especificado pelos argumentos  *Em*  e  *Condição Where*  especificar mais de um registro, o bloco de dados **PesquisarRegistro** será executado somente no primeiro registro.</span><span class="sxs-lookup"><span data-stu-id="526a7-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="526a7-130">Se nenhum registro satisfizer *Condição Where* ou *se não tiver registros* , **Pesquisarregistro** cria um registro em branco no qual todos os campos contêm um valor **Nulo** .</span><span class="sxs-lookup"><span data-stu-id="526a7-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

