---
title: Agrupar e restringir tabelas em provedores do repositório de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 33c76cdd0e7850f82949349ac2e5bb0dd4e056ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766664"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="01b0f-103">Agrupar e restringir tabelas em provedores do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="01b0f-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="01b0f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01b0f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01b0f-105">Aplicativos de cliente com frequência permitem aos usuários algum controle sobre como o conteúdo de uma pasta é exibido.</span><span class="sxs-lookup"><span data-stu-id="01b0f-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="01b0f-106">Normalmente, um usuário pode optar por mensagens agrupados de acordo com o valor de uma ou mais propriedades de mensagem, ou pode optar por excluir mensagens que correspondem a determinados critérios.</span><span class="sxs-lookup"><span data-stu-id="01b0f-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="01b0f-107">Isso é feito usando o [IMAPITable: IUnknown](imapitableiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="01b0f-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="01b0f-108">Aplicativos cliente podem restringir as linhas retornadas da tabela para todos os critérios que o usuário especifica.</span><span class="sxs-lookup"><span data-stu-id="01b0f-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="01b0f-109">Portanto, uma mensagem armazene as necessidades do provedor para implementar os seguintes métodos **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="01b0f-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="01b0f-110">IMAPITable * * método * *</span><span class="sxs-lookup"><span data-stu-id="01b0f-110">****IMAPITable** method**</span></span>|<span data-ttu-id="01b0f-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="01b0f-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01b0f-112">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="01b0f-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="01b0f-113">Retorna a tabela linhas que coincidem com os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="01b0f-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="01b0f-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="01b0f-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="01b0f-115">Retorna o conjunto de colunas em uma tabela ou o conjunto de colunas atualmente em uso.</span><span class="sxs-lookup"><span data-stu-id="01b0f-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="01b0f-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="01b0f-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="01b0f-117">Retorna uma ou mais linhas de uma tabela, iniciando a partir de uma determinada posição.</span><span class="sxs-lookup"><span data-stu-id="01b0f-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="01b0f-118">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="01b0f-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="01b0f-119">Aplica uma restrição a uma tabela para que as chamadas subsequentes **FindRow** retornam somente as linhas que coincidem com a restrição.</span><span class="sxs-lookup"><span data-stu-id="01b0f-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="01b0f-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="01b0f-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="01b0f-121">Especifica quais colunas devem ser retornadas quando linhas são recuperadas da tabela.</span><span class="sxs-lookup"><span data-stu-id="01b0f-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="01b0f-122">Restrições podem ser complexas para implementar; Para obter mais informações, consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="01b0f-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="01b0f-123">Para obter mais informações sobre como implementar as tabelas, consulte [As tabelas de MAPI](mapi-tables.md).</span><span class="sxs-lookup"><span data-stu-id="01b0f-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="01b0f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="01b0f-124">See also</span></span>



[<span data-ttu-id="01b0f-125">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="01b0f-125">Message Store Features</span></span>](message-store-features.md)

