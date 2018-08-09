---
title: Recuperar dados das linhas de tabelas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19a42794-a3a2-4336-af2a-473f24431252
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 91b1fa06fd47321e9c19d9751caac793e27e8f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770263"
---
# <a name="retrieving-data-from-table-rows"></a><span data-ttu-id="df277-103">Recuperar dados das linhas de tabelas</span><span class="sxs-lookup"><span data-stu-id="df277-103">Retrieving Data from Table Rows</span></span>

  
  
<span data-ttu-id="df277-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df277-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df277-105">Recuperação de linhas de uma tabela envolve:</span><span class="sxs-lookup"><span data-stu-id="df277-105">Retrieving rows from a table involves:</span></span>
  
- <span data-ttu-id="df277-106">Obtendo os valores de propriedade para todas as colunas.</span><span class="sxs-lookup"><span data-stu-id="df277-106">Obtaining the property values for all the columns.</span></span>
    
- <span data-ttu-id="df277-107">Modificando a posição atual.</span><span class="sxs-lookup"><span data-stu-id="df277-107">Modifying the current position.</span></span>
    
<span data-ttu-id="df277-108">Uma das colunas necessárias na maioria das tabelas é um identificador de entrada — a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) — que pode ser usado para abrir o objeto que representa a linha.</span><span class="sxs-lookup"><span data-stu-id="df277-108">One of the required columns in most tables is an entry identifier — the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property — that can be used to open the object that represents the row.</span></span> <span data-ttu-id="df277-109">Geralmente, esse identificador de entrada é um identificador curto prazo de entrada, que não persiste passou a vida útil da tabela.</span><span class="sxs-lookup"><span data-stu-id="df277-109">This entry identifier is usually a short-term entry identifier, one that does not persist past the lifetime of the table.</span></span> <span data-ttu-id="df277-110">No entanto, ele pode ser um identificador de longo prazo, se o provedor de serviço implementando a tabela só oferece suporte a um tipo de identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="df277-110">However, it can be a long-term identifier if the service provider implementing the table only supports one type of entry identifier.</span></span>
  
<span data-ttu-id="df277-111">Clientes e provedores de serviços podem fazer uma das seguintes chamadas para recuperar linhas:</span><span class="sxs-lookup"><span data-stu-id="df277-111">Clients and service providers can make one of the following calls to retrieve rows:</span></span>
  
|||
|:-----|:-----|
|[<span data-ttu-id="df277-112">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="df277-112">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="df277-113">Recupera um número especificado de linhas, começando com a linha atual na direção frente ou para trás.</span><span class="sxs-lookup"><span data-stu-id="df277-113">Retrieves a specified number of rows starting with the current row in either a forward or backward direction.</span></span>  <br/> |
|[<span data-ttu-id="df277-114">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="df277-114">HrQueryAllRows</span></span>](hrqueryallrows.md) <br/> |<span data-ttu-id="df277-115">Recupera todas as linhas em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="df277-115">Retrieves all of the rows in a table.</span></span>  <br/> |
|[<span data-ttu-id="df277-116">ITableData::HrQueryRow</span><span class="sxs-lookup"><span data-stu-id="df277-116">ITableData::HrQueryRow</span></span>](itabledata-hrqueryrow.md) <br/> |<span data-ttu-id="df277-117">Recupera uma linha em uma tabela de acordo com o valor da coluna seu índice.</span><span class="sxs-lookup"><span data-stu-id="df277-117">Retrieves a row in a table according to the value of its index column.</span></span> <span data-ttu-id="df277-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) é geralmente a coluna de índice para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="df277-118">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) is usually the index column for a table.</span></span>  <br/> |
   
<span data-ttu-id="df277-119">Quando uma propriedade opcional é incluída como uma das colunas em uma tabela, algumas das linhas podem ter os valores válidos para a coluna, enquanto outros usuários talvez não.</span><span class="sxs-lookup"><span data-stu-id="df277-119">When an optional property is included as one of the columns in a table, some of the rows might have valid values for the column while others might not.</span></span> <span data-ttu-id="df277-120">Se um valor válido existe para uma coluna depende se o objeto fornecendo as informações para a linha define a propriedade.</span><span class="sxs-lookup"><span data-stu-id="df277-120">Whether a valid value exists for a column depends on whether the object providing the information for the row sets the property.</span></span> <span data-ttu-id="df277-121">Dependendo da implementação do objeto, uma propriedade inexistentes pode ser representada na tabela como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) ou um valor arbitrário.</span><span class="sxs-lookup"><span data-stu-id="df277-121">Depending on the implementation of the object, a non-existent property can be represented in the table as **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) or an arbitrary value.</span></span> <span data-ttu-id="df277-122">Os usuários das tabelas devem tomar cuidadosos diferenciar entre as propriedades que são inexistente e têm valores insignificante e que existem e têm valores válidos.</span><span class="sxs-lookup"><span data-stu-id="df277-122">Users of tables must be careful to differentiate between properties that are nonexistent and have meaningless values and properties that do exist and have valid values.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="df277-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="df277-123">See also</span></span>



[<span data-ttu-id="df277-124">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="df277-124">MAPI Tables</span></span>](mapi-tables.md)

