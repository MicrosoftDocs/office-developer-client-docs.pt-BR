---
title: Agrupar e restringir tabelas em provedores de repositórios de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299409"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="57ae4-103">Agrupar e restringir tabelas em provedores de repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="57ae4-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="57ae4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57ae4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57ae4-105">Os aplicativos cliente freqüentemente permitem que os usuários tenham controle sobre como o conteúdo de uma pasta é exibido.</span><span class="sxs-lookup"><span data-stu-id="57ae4-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="57ae4-106">Normalmente, um usuário pode optar por ter mensagens agrupadas de acordo com o valor de uma ou mais propriedades de mensagem, ou pode optar por excluir mensagens que correspondam a determinados critérios.</span><span class="sxs-lookup"><span data-stu-id="57ae4-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="57ae4-107">Isso é feito usando a interface [IMAPITable: IUnknown](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="57ae4-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="57ae4-108">Os aplicativos cliente podem restringir as linhas retornadas da tabela para qualquer critério especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="57ae4-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="57ae4-109">Portanto, um provedor de repositório de mensagens precisa implementar os \*\*\*\* métodos IMAPITable a seguir.</span><span class="sxs-lookup"><span data-stu-id="57ae4-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="57ae4-110">ImApitable \* \* método \* \*</span><span class="sxs-lookup"><span data-stu-id="57ae4-110">\*\*\*\*IMAPITable\*\* method\*\*</span></span>|<span data-ttu-id="57ae4-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="57ae4-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57ae4-112">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="57ae4-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="57ae4-113">Retorna linhas de tabela que correspondem aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="57ae4-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="57ae4-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="57ae4-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="57ae4-115">Retorna o conjunto de colunas em uma tabela ou o conjunto de colunas usadas no momento.</span><span class="sxs-lookup"><span data-stu-id="57ae4-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="57ae4-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="57ae4-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="57ae4-117">Retorna uma ou mais linhas de uma tabela, começando a partir de uma determinada posição.</span><span class="sxs-lookup"><span data-stu-id="57ae4-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="57ae4-118">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="57ae4-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="57ae4-119">Aplica uma restrição a uma tabela para que chamadas subsequentes para o **FindRow** retornem somente as linhas que correspondem à restrição.</span><span class="sxs-lookup"><span data-stu-id="57ae4-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="57ae4-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="57ae4-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="57ae4-121">Especifica quais colunas devem ser retornadas quando as linhas são recuperadas da tabela.</span><span class="sxs-lookup"><span data-stu-id="57ae4-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="57ae4-122">As restrições podem ser complexas para implementar; para obter mais informações, consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="57ae4-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="57ae4-123">Para obter mais informações sobre a implementação de tabelas, consulte [tabelas MAPI](mapi-tables.md).</span><span class="sxs-lookup"><span data-stu-id="57ae4-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57ae4-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="57ae4-124">See also</span></span>



[<span data-ttu-id="57ae4-125">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="57ae4-125">Message Store Features</span></span>](message-store-features.md)

