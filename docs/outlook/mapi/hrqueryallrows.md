---
title: HrQueryAllRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrQueryAllRows
api_type:
- HeaderDef
ms.assetid: b08fadcf-cdf3-48b7-9489-d7f745266482
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5c62e5919c6e605aa4b60f48072996ed1fd4c355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766809"
---
# <a name="hrqueryallrows"></a><span data-ttu-id="7bd5f-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="7bd5f-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="7bd5f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7bd5f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7bd5f-105">Recupera todas as linhas de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7bd5f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7bd5f-106">Header file:</span></span>  <br/> |<span data-ttu-id="7bd5f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7bd5f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7bd5f-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="7bd5f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7bd5f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7bd5f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7bd5f-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="7bd5f-110">Called by:</span></span>  <br/> |<span data-ttu-id="7bd5f-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="7bd5f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrQueryAllRows(
  LPMAPITABLE ptable,
  LPSPropTagArray ptaga,
  LPSRestriction pres,
  LPSSortOrderSet psos,
  LONG crowsMax,
  LPSRowSet FAR * pprows
);
```

## <a name="parameters"></a><span data-ttu-id="7bd5f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bd5f-112">Parameters</span></span>

 <span data-ttu-id="7bd5f-113">_ptable_</span><span class="sxs-lookup"><span data-stu-id="7bd5f-113">_ptable_</span></span>
  
> <span data-ttu-id="7bd5f-114">[in] Ponteiro para a tabela MAPI do qual as linhas são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="7bd5f-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="7bd5f-115">_ptaga_</span></span>
  
> <span data-ttu-id="7bd5f-116">[in] Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de propriedade marcas indicando colunas da tabela.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="7bd5f-117">Essas marcas são usadas para selecionar as colunas específicas a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="7bd5f-118">Se o parâmetro _ptaga_ for NULL, **HrQueryAllRows** recupera o conjunto de coluna inteira do modo de exibição de tabela atual passado no parâmetro _ptable_ .</span><span class="sxs-lookup"><span data-stu-id="7bd5f-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="7bd5f-119">_pré-instalação_</span><span class="sxs-lookup"><span data-stu-id="7bd5f-119">_pres_</span></span>
  
> <span data-ttu-id="7bd5f-120">[in] Ponteiro para uma estrutura [SRestriction](srestriction.md) que contém as restrições de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="7bd5f-121">Se o parâmetro de _pré-instalação_ for NULL, **HrQueryAllRows** torna sem restrições.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="7bd5f-122">_PSOs_</span><span class="sxs-lookup"><span data-stu-id="7bd5f-122">_psos_</span></span>
  
> <span data-ttu-id="7bd5f-123">[in] Ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que identifica a ordem de classificação das colunas a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="7bd5f-124">Se o parâmetro _psos_ for NULL, a ordem de classificação padrão para a tabela será usada.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="7bd5f-125">_crowsMax_</span><span class="sxs-lookup"><span data-stu-id="7bd5f-125">_crowsMax_</span></span>
  
> <span data-ttu-id="7bd5f-126">[in] Número máximo de linhas a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="7bd5f-127">Se o valor do parâmetro _crowsMax_ for zero, nenhum limite no número de linhas recuperadas é definido.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="7bd5f-128">_pprows_</span><span class="sxs-lookup"><span data-stu-id="7bd5f-128">_pprows_</span></span>
  
> <span data-ttu-id="7bd5f-129">[out] Ponteiro para um ponteiro para a estrutura [SRowSet](srowset.md) retornado que contém uma matriz de ponteiros para as linhas de tabela recuperadas.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7bd5f-130">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7bd5f-130">Return value</span></span>

<span data-ttu-id="7bd5f-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="7bd5f-131">S_OK</span></span> 
  
> <span data-ttu-id="7bd5f-132">A chamada recuperado as linhas esperadas de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="7bd5f-133">MAPI_E_TABLE_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="7bd5f-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="7bd5f-134">O número de linhas da tabela é maior que o número passado para o parâmetro _crowsMax_ .</span><span class="sxs-lookup"><span data-stu-id="7bd5f-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7bd5f-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bd5f-135">Remarks</span></span>

<span data-ttu-id="7bd5f-136">Um aplicativo cliente ou um provedor de serviços não tem controle sobre o número de linhas **que HrQueryAllRows** tenta recuperar, diferente de, impondo uma restrição apontado pelo parâmetro _pré-instalação_ .</span><span class="sxs-lookup"><span data-stu-id="7bd5f-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="7bd5f-137">O parâmetro _crowsMax_ não limitam a recuperação para um determinado número de linhas da tabela, mas em vez disso, define uma quantidade máxima de memória disponível para abrigar recuperadas todas as linhas.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="7bd5f-138">A única proteção contra estouro de memória enorme é o recurso de provisórias fornecido, definindo _crowsMax_.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="7bd5f-139">O retorno de erro MAPI_E_TABLE_TOO_BIG significa que a tabela contém muitas linhas seja mantido todo ao mesmo tempo na memória.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="7bd5f-140">Tabelas que são normalmente pequenas, como uma tabela de repositório de mensagens ou de uma tabela de provedor, geralmente podem ser com segurança recuperadas com **HrQueryAllRows**.</span><span class="sxs-lookup"><span data-stu-id="7bd5f-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="7bd5f-141">Tabelas em risco de ser muito grande, como uma tabela de conteúdo ou até mesmo uma tabela de destinatários, devem ser percorridas nas subseções usando o método [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="7bd5f-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="7bd5f-142">Se houver qualquer tabela propriedades indefinidas quando **HrQueryAllRows** é chamado, são retornadas com o tipo de propriedade PT_NULL e o identificador de propriedade PROP_ID_NULL</span><span class="sxs-lookup"><span data-stu-id="7bd5f-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

