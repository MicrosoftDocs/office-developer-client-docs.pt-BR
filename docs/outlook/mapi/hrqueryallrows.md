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
ms.openlocfilehash: 0f09304f21180d9ebc2a1e1dcc54ebadd3622804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422891"
---
# <a name="hrqueryallrows"></a><span data-ttu-id="b796c-103">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="b796c-103">HrQueryAllRows</span></span>

  
  
<span data-ttu-id="b796c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b796c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b796c-105">Recupera todas as linhas de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="b796c-105">Retrieves all rows of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b796c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b796c-106">Header file:</span></span>  <br/> |<span data-ttu-id="b796c-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="b796c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b796c-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b796c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b796c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b796c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b796c-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="b796c-110">Called by:</span></span>  <br/> |<span data-ttu-id="b796c-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="b796c-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="b796c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b796c-112">Parameters</span></span>

 <span data-ttu-id="b796c-113">_PTable_</span><span class="sxs-lookup"><span data-stu-id="b796c-113">_ptable_</span></span>
  
> <span data-ttu-id="b796c-114">no Ponteiro para a tabela MAPI da qual as linhas são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="b796c-114">[in] Pointer to the MAPI table from which rows are retrieved.</span></span> 
    
 <span data-ttu-id="b796c-115">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="b796c-115">_ptaga_</span></span>
  
> <span data-ttu-id="b796c-116">no Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que indicam as colunas da tabela.</span><span class="sxs-lookup"><span data-stu-id="b796c-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating table columns.</span></span> <span data-ttu-id="b796c-117">Essas marcas são usadas para selecionar as colunas específicas a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="b796c-117">These tags are used to select the specific columns to be retrieved.</span></span> <span data-ttu-id="b796c-118">Se o parâmetro _ptaga_ for NULL, **HrQueryAllRows** recuperará todo o conjunto de colunas do modo de exibição de tabela atual passado no parâmetro _PTable_ .</span><span class="sxs-lookup"><span data-stu-id="b796c-118">If the  _ptaga_ parameter is NULL, **HrQueryAllRows** retrieves the entire column set of the current table view passed in the  _ptable_ parameter.</span></span> 
    
 <span data-ttu-id="b796c-119">_pré-instalação_</span><span class="sxs-lookup"><span data-stu-id="b796c-119">_pres_</span></span>
  
> <span data-ttu-id="b796c-120">no Ponteiro para uma estrutura [SRestriction](srestriction.md) que contém restrições de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b796c-120">[in] Pointer to an [SRestriction](srestriction.md) structure that contains retrieval restrictions.</span></span> <span data-ttu-id="b796c-121">Se o parâmetro _Pres_ for NULL, **HrQueryAllRows** não fará nenhuma restrição.</span><span class="sxs-lookup"><span data-stu-id="b796c-121">If the  _pres_ parameter is NULL, **HrQueryAllRows** makes no restrictions.</span></span> 
    
 <span data-ttu-id="b796c-122">_PSOs_</span><span class="sxs-lookup"><span data-stu-id="b796c-122">_psos_</span></span>
  
> <span data-ttu-id="b796c-123">no Ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) identificando a ordem de classificação das colunas a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="b796c-123">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order of the columns to be retrieved.</span></span> <span data-ttu-id="b796c-124">Se o parâmetro _PSOs_ for NULL, a ordem de classificação padrão para a tabela será usada.</span><span class="sxs-lookup"><span data-stu-id="b796c-124">If the  _psos_ parameter is NULL, the default sort order for the table is used.</span></span> 
    
 <span data-ttu-id="b796c-125">_crowsMax_</span><span class="sxs-lookup"><span data-stu-id="b796c-125">_crowsMax_</span></span>
  
> <span data-ttu-id="b796c-126">no Número máximo de linhas a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="b796c-126">[in] Maximum number of rows to be retrieved.</span></span> <span data-ttu-id="b796c-127">Se o valor do parâmetro _crowsMax_ for zero, nenhum limite no número de linhas recuperadas será definido.</span><span class="sxs-lookup"><span data-stu-id="b796c-127">If the value of the  _crowsMax_ parameter is zero, no limit on the number of rows retrieved is set.</span></span> 
    
 <span data-ttu-id="b796c-128">_pprows_</span><span class="sxs-lookup"><span data-stu-id="b796c-128">_pprows_</span></span>
  
> <span data-ttu-id="b796c-129">bota Ponteiro para um ponteiro para a estrutura [SRowSet](srowset.md) retornada que contém uma matriz de ponteiros para as linhas da tabela recuperadas.</span><span class="sxs-lookup"><span data-stu-id="b796c-129">[out] Pointer to a pointer to the returned [SRowSet](srowset.md) structure that contains an array of pointers to the retrieved table rows.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b796c-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b796c-130">Return value</span></span>

<span data-ttu-id="b796c-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="b796c-131">S_OK</span></span> 
  
> <span data-ttu-id="b796c-132">A chamada recuperou as linhas esperadas de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="b796c-132">The call retrieved the expected rows of a table.</span></span> 
    
<span data-ttu-id="b796c-133">MAPI_E_TABLE_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="b796c-133">MAPI_E_TABLE_TOO_BIG</span></span> 
  
> <span data-ttu-id="b796c-134">O número de linhas na tabela é maior do que o número passado para o parâmetro _crowsMax_ .</span><span class="sxs-lookup"><span data-stu-id="b796c-134">The number of rows in the table is larger than the number passed for the  _crowsMax_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b796c-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="b796c-135">Remarks</span></span>

<span data-ttu-id="b796c-136">Um aplicativo cliente ou provedor de serviços não tem controle sobre o número de linhas que o **HrQueryAllRows** tenta recuperar, exceto por impor uma restrição apontada pelo parâmetro _Pres_ .</span><span class="sxs-lookup"><span data-stu-id="b796c-136">A client application or service provider has no control over the number of rows **HrQueryAllRows** attempts to retrieve, other than by imposing a restriction pointed to by the  _pres_ parameter.</span></span> <span data-ttu-id="b796c-137">O parâmetro _crowsMax_ não limita a recuperação a um determinado número de linhas de tabela, mas, em vez disso, define uma quantidade máxima de memória disponível para armazenar todas as linhas recuperadas.</span><span class="sxs-lookup"><span data-stu-id="b796c-137">The  _crowsMax_ parameter does not limit the retrieval to a certain number of table rows, but rather defines a maximum amount of memory available to hold all retrieved rows.</span></span> <span data-ttu-id="b796c-138">A única proteção contra estouro de memória maciça é o recurso stopgap fornecido pela configuração _crowsMax_.</span><span class="sxs-lookup"><span data-stu-id="b796c-138">The only protection against massive memory overflow is the stopgap feature provided by setting  _crowsMax_.</span></span> <span data-ttu-id="b796c-139">O erro de retorno MAPI_E_TABLE_TOO_BIG significa que a tabela contém muitas linhas a serem mantidas de uma só vez na memória.</span><span class="sxs-lookup"><span data-stu-id="b796c-139">The error return MAPI_E_TABLE_TOO_BIG means the table contains too many rows to be held all at once in memory.</span></span> 
  
<span data-ttu-id="b796c-140">As tabelas que são normalmente pequenas, como uma tabela de repositório de mensagens ou uma tabela de provedor, geralmente podem ser recuperadas com segurança com o **HrQueryAllRows**.</span><span class="sxs-lookup"><span data-stu-id="b796c-140">Tables that are typically small, such as a message store table or a provider table, usually can be safely retrieved with **HrQueryAllRows**.</span></span> <span data-ttu-id="b796c-141">As tabelas em risco de ser muito grande, como uma tabela de conteúdo ou mesmo uma tabela de destinatários, devem ser percorridas em subseções usando o método imApitable [:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="b796c-141">Tables at risk of being very large, such as a contents table or even a recipients table, should be traversed in subsections using the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> 
  
<span data-ttu-id="b796c-142">Se qualquer propriedade da tabela estiver indefinida quando **HrQueryAllRows** for chamado, elas serão retornadas com o tipo de propriedade PT_NULL e o identificador de propriedade PROP_ID_NULL</span><span class="sxs-lookup"><span data-stu-id="b796c-142">If any table properties are undefined when **HrQueryAllRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL</span></span> 
  

