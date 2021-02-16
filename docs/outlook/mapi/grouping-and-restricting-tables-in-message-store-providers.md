---
title: Agrupando e restringindo tabelas em provedores de armazenamento de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01df4be4-98a1-4159-a06d-9ccf4337198f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8a45a9fd0d40c16d110fd52be1ac1117e1dd4d04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428981"
---
# <a name="grouping-and-restricting-tables-in-message-store-providers"></a><span data-ttu-id="2b291-103">Agrupando e restringindo tabelas em provedores de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="2b291-103">Grouping and Restricting Tables in Message Store Providers</span></span>

  
  
<span data-ttu-id="2b291-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b291-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b291-105">Frequentemente, os aplicativos cliente permitem aos usuários algum controle sobre como o conteúdo de uma pasta é exibido.</span><span class="sxs-lookup"><span data-stu-id="2b291-105">Client applications frequently allow users some control over how the contents of a folder are displayed.</span></span> <span data-ttu-id="2b291-106">Normalmente, um usuário pode optar por ter mensagens agrupadas de acordo com o valor de uma ou mais propriedades da mensagem ou pode optar por excluir mensagens que corresponderem a determinados critérios.</span><span class="sxs-lookup"><span data-stu-id="2b291-106">Typically, a user can choose to have messages grouped according to the value of one or more message properties, or can choose to exclude messages that match certain criteria.</span></span> <span data-ttu-id="2b291-107">Isso é feito usando a interface [IMAPITable : IUnknown.](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="2b291-107">This is done by using the [IMAPITable : IUnknown](imapitableiunknown.md) interface.</span></span> <span data-ttu-id="2b291-108">Os aplicativos cliente podem restringir as linhas retornadas da tabela a qualquer critério especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2b291-108">Client applications can restrict the rows returned from the table to whatever criteria the user specifies.</span></span> <span data-ttu-id="2b291-109">Portanto, um provedor de armazenamento de mensagens precisa implementar os métodos **IMAPITable** a seguir.</span><span class="sxs-lookup"><span data-stu-id="2b291-109">Therefore, a message store provider needs to implement the following **IMAPITable** methods.</span></span> 
  
|<span data-ttu-id="2b291-110">Método IMAPITable\*\*</span><span class="sxs-lookup"><span data-stu-id="2b291-110">\*\*\*\*IMAPITable\*\* method\*\*</span></span>|<span data-ttu-id="2b291-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2b291-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b291-112">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="2b291-112">IMAPITable::FindRow</span></span>](imapitable-findrow.md) <br/> |<span data-ttu-id="2b291-113">Retorna linhas de tabela que corresponderem aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="2b291-113">Returns table rows that match the specified criteria.</span></span>  <br/> |
|[<span data-ttu-id="2b291-114">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="2b291-114">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md) <br/> |<span data-ttu-id="2b291-115">Retorna o conjunto de colunas em uma tabela ou o conjunto de colunas usadas no momento.</span><span class="sxs-lookup"><span data-stu-id="2b291-115">Returns the set of columns in a table or the set of currently used columns.</span></span>  <br/> |
|[<span data-ttu-id="2b291-116">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="2b291-116">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md) <br/> |<span data-ttu-id="2b291-117">Retorna uma ou mais linhas de uma tabela, começando de uma determinada posição.</span><span class="sxs-lookup"><span data-stu-id="2b291-117">Returns one or more rows from a table, starting from a given position.</span></span>  <br/> |
|[<span data-ttu-id="2b291-118">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="2b291-118">IMAPITable::Restrict</span></span>](imapitable-restrict.md) <br/> |<span data-ttu-id="2b291-119">Aplica uma restrição a uma tabela para que as chamadas subsequentes para **FindRow** retornem apenas linhas que corresponderem à restrição.</span><span class="sxs-lookup"><span data-stu-id="2b291-119">Applies a restriction to a table so that subsequent calls to **FindRow** return only rows that match the restriction.</span></span>  <br/> |
|[<span data-ttu-id="2b291-120">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="2b291-120">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md) <br/> |<span data-ttu-id="2b291-121">Especifica quais colunas devem ser retornadas quando as linhas são recuperadas da tabela.</span><span class="sxs-lookup"><span data-stu-id="2b291-121">Specifies which columns should be returned when rows are retrieved from the table.</span></span>  <br/> |
   
<span data-ttu-id="2b291-122">As restrições podem ser complexas de implementar; para obter mais informações, consulte [Sobre restrições.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="2b291-122">Restrictions can be complex to implement; for more information, see [About Restrictions](about-restrictions.md).</span></span> <span data-ttu-id="2b291-123">Para obter mais informações sobre como implementar tabelas, consulte [tabelas MAPI](mapi-tables.md).</span><span class="sxs-lookup"><span data-stu-id="2b291-123">For more information about implementing tables, see [MAPI Tables](mapi-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2b291-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b291-124">See also</span></span>



[<span data-ttu-id="2b291-125">Recursos do Armazenamento de Mensagens</span><span class="sxs-lookup"><span data-stu-id="2b291-125">Message Store Features</span></span>](message-store-features.md)

