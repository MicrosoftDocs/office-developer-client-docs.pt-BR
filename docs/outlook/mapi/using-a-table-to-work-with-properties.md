---
title: Usar uma tabela para trabalhar com propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e4e7ecda40f3f3fcb05700ba3e8b79ab21cbe35b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770681"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="c6fdb-103">Usar uma tabela para trabalhar com propriedades</span><span class="sxs-lookup"><span data-stu-id="c6fdb-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="c6fdb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6fdb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c6fdb-105">Muitas propriedades estão disponíveis nos objetos que dão suporte a eles e como colunas nas tabelas.</span><span class="sxs-lookup"><span data-stu-id="c6fdb-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="c6fdb-106">Sempre que possível, recupere essas propriedades por meio da tabela.</span><span class="sxs-lookup"><span data-stu-id="c6fdb-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="c6fdb-107">Chamadas [IMAPITable::SetColumns](imapitable-setcolumns.md) para incluir todas as propriedades que precisa de seu cliente e [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas as linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="c6fdb-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="c6fdb-108">Essas duas chamadas geralmente são suficientes para recuperar informações suficientes para exibir a um usuário e são frequentemente suficientes para qualquer processamento interno necessário, fazendo uma chamada para **OpenEntry** para abrir o objeto desnecessário.</span><span class="sxs-lookup"><span data-stu-id="c6fdb-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="c6fdb-109">Existem apenas duas exceções:</span><span class="sxs-lookup"><span data-stu-id="c6fdb-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="c6fdb-110">Se a propriedade for com mais de 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="c6fdb-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="c6fdb-111">O * * IMAPITable * * interface não pode retornar o valor da propriedade inteira, em vez disso, truncá-la em 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="c6fdb-111">The ** IMAPITable ** interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="c6fdb-112">Pense essa compensação, no entanto.</span><span class="sxs-lookup"><span data-stu-id="c6fdb-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="c6fdb-113">Se você estiver exibindo esses dados para o usuário, 255 bytes pode ser suficiente para que um campo textual como um comentário.</span><span class="sxs-lookup"><span data-stu-id="c6fdb-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="c6fdb-114">Se você precisa de uma propriedade específica de uma única linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="c6fdb-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="c6fdb-115">Nesse caso é desnecessário criar uma tabela com propriedades que nunca serão usadas.</span><span class="sxs-lookup"><span data-stu-id="c6fdb-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="c6fdb-116">Na maioria das vezes você precisará as mesmas propriedades para todas as linhas.</span><span class="sxs-lookup"><span data-stu-id="c6fdb-116">Most of the time you will need the same properties for all rows.</span></span>
    

