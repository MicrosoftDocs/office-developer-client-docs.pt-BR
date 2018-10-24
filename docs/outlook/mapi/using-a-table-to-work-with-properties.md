---
title: Usar uma tabela para trabalhar com propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9f02da9eb1920f55acf65dfb6a503e42d4c3daf2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585420"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="f1c2b-103">Usar uma tabela para trabalhar com propriedades</span><span class="sxs-lookup"><span data-stu-id="f1c2b-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="f1c2b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1c2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1c2b-105">Muitas propriedades estão disponíveis nos objetos que dão suporte a eles e como colunas nas tabelas.</span><span class="sxs-lookup"><span data-stu-id="f1c2b-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="f1c2b-106">Sempre que possível, recupere essas propriedades por meio da tabela.</span><span class="sxs-lookup"><span data-stu-id="f1c2b-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="f1c2b-107">Chamadas [IMAPITable::SetColumns](imapitable-setcolumns.md) para incluir todas as propriedades que precisa de seu cliente e [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas as linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="f1c2b-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="f1c2b-108">Essas duas chamadas geralmente são suficientes para recuperar informações suficientes para exibir a um usuário e são frequentemente suficientes para qualquer processamento interno necessário, fazendo uma chamada para **OpenEntry** para abrir o objeto desnecessário.</span><span class="sxs-lookup"><span data-stu-id="f1c2b-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="f1c2b-109">Existem apenas duas exceções:</span><span class="sxs-lookup"><span data-stu-id="f1c2b-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="f1c2b-110">Se a propriedade for com mais de 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="f1c2b-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="f1c2b-111">O \* \* IMAPITable \* \* interface não pode retornar o valor da propriedade inteira, em vez disso, truncá-la em 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="f1c2b-111">The \*\* IMAPITable \*\* interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="f1c2b-112">Pense essa compensação, no entanto.</span><span class="sxs-lookup"><span data-stu-id="f1c2b-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="f1c2b-113">Se você estiver exibindo esses dados para o usuário, 255 bytes pode ser suficiente para que um campo textual como um comentário.</span><span class="sxs-lookup"><span data-stu-id="f1c2b-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="f1c2b-114">Se você precisa de uma propriedade específica de uma única linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="f1c2b-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="f1c2b-115">Nesse caso é desnecessário criar uma tabela com propriedades que nunca serão usadas.</span><span class="sxs-lookup"><span data-stu-id="f1c2b-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="f1c2b-116">Na maioria das vezes você precisará as mesmas propriedades para todas as linhas.</span><span class="sxs-lookup"><span data-stu-id="f1c2b-116">Most of the time you will need the same properties for all rows.</span></span>
    

