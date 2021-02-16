---
title: Recuperando dados de linhas de tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2f389d26ec80b9af3ed28c5eb85b589c9cbb26c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405251"
---
# <a name="retrieving-data-from-table-rows"></a><span data-ttu-id="68a23-103">Recuperando dados de linhas de tabela</span><span class="sxs-lookup"><span data-stu-id="68a23-103">Retrieving Data from Table Rows</span></span>

  
  
<span data-ttu-id="68a23-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68a23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68a23-105">Recuperar linhas de uma tabela envolve:</span><span class="sxs-lookup"><span data-stu-id="68a23-105">Retrieving rows from a table involves:</span></span>
  
- <span data-ttu-id="68a23-106">Obtendo os valores de propriedade para todas as colunas.</span><span class="sxs-lookup"><span data-stu-id="68a23-106">Obtaining the property values for all the columns.</span></span>
    
- <span data-ttu-id="68a23-107">Modificando a posição atual.</span><span class="sxs-lookup"><span data-stu-id="68a23-107">Modifying the current position.</span></span>
    
<span data-ttu-id="68a23-108">Uma das colunas necessárias na maioria das tabelas é um identificador de entrada — a propriedade PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) — que pode ser usada para abrir o objeto que representa **a** linha.</span><span class="sxs-lookup"><span data-stu-id="68a23-108">One of the required columns in most tables is an entry identifier — the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property — that can be used to open the object that represents the row.</span></span> <span data-ttu-id="68a23-109">Esse identificador de entrada geralmente é um identificador de entrada de curto prazo, que não persiste após o tempo de vida da tabela.</span><span class="sxs-lookup"><span data-stu-id="68a23-109">This entry identifier is usually a short-term entry identifier, one that does not persist past the lifetime of the table.</span></span> <span data-ttu-id="68a23-110">No entanto, ele pode ser um identificador de longo prazo se o provedor de serviços que implementa a tabela suporta apenas um tipo de identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="68a23-110">However, it can be a long-term identifier if the service provider implementing the table only supports one type of entry identifier.</span></span>
  
<span data-ttu-id="68a23-111">Os clientes e provedores de serviços podem fazer uma das seguintes chamadas para recuperar linhas:</span><span class="sxs-lookup"><span data-stu-id="68a23-111">Clients and service providers can make one of the following calls to retrieve rows:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="68a23-112">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="68a23-112">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="68a23-113">Recupera um número especificado de linhas começando com a linha atual em uma direção para frente ou para trás.</span><span class="sxs-lookup"><span data-stu-id="68a23-113">Retrieves a specified number of rows starting with the current row in either a forward or backward direction.</span></span>  <br/> |
|[<span data-ttu-id="68a23-114">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="68a23-114">HrQueryAllRows</span></span>](hrqueryallrows.md) <br/> |<span data-ttu-id="68a23-115">Recupera todas as linhas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="68a23-115">Retrieves all of the rows in a table.</span></span>  <br/> |
|[<span data-ttu-id="68a23-116">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="68a23-116">ITableData::HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="68a23-117">Recupera uma linha em uma tabela de acordo com o valor de sua coluna de índice.</span><span class="sxs-lookup"><span data-stu-id="68a23-117">Retrieves a row in a table according to the value of its index column.</span></span> <span data-ttu-id="68a23-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) geralmente é a coluna de índice de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="68a23-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) is usually the index column for a table.</span></span>  <br/> |
   
<span data-ttu-id="68a23-119">Quando uma propriedade opcional é incluída como uma das colunas em uma tabela, algumas das linhas podem ter valores válidos para a coluna, enquanto outras podem não ter.</span><span class="sxs-lookup"><span data-stu-id="68a23-119">When an optional property is included as one of the columns in a table, some of the rows might have valid values for the column while others might not.</span></span> <span data-ttu-id="68a23-120">Se existe um valor válido para uma coluna depende se o objeto que fornece as informações para a linha define a propriedade.</span><span class="sxs-lookup"><span data-stu-id="68a23-120">Whether a valid value exists for a column depends on whether the object providing the information for the row sets the property.</span></span> <span data-ttu-id="68a23-121">Dependendo da implementação do objeto, uma propriedade inexistente pode ser representada na tabela como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ou um valor arbitrário.</span><span class="sxs-lookup"><span data-stu-id="68a23-121">Depending on the implementation of the object, a non-existent property can be represented in the table as **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) or an arbitrary value.</span></span> <span data-ttu-id="68a23-122">Os usuários de tabelas devem ter cuidado para diferenciar entre propriedades que não são inexistentes e têm valores e propriedades sem sentido que existem e têm valores válidos.</span><span class="sxs-lookup"><span data-stu-id="68a23-122">Users of tables must be careful to differentiate between properties that are nonexistent and have meaningless values and properties that do exist and have valid values.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="68a23-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="68a23-123">See also</span></span>



[<span data-ttu-id="68a23-124">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="68a23-124">MAPI Tables</span></span>](mapi-tables.md)

