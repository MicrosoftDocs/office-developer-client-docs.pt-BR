---
title: Usando uma tabela para trabalhar com propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 59196f136c422be912ac2460cbbd25d8bc2e3330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439909"
---
# <a name="using-a-table-to-work-with-properties"></a><span data-ttu-id="ca71a-103">Usando uma tabela para trabalhar com propriedades</span><span class="sxs-lookup"><span data-stu-id="ca71a-103">Using a Table to Work with Properties</span></span>

  
  
<span data-ttu-id="ca71a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca71a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca71a-105">Muitas propriedades estão disponíveis nos objetos que as suportam e como colunas em tabelas.</span><span class="sxs-lookup"><span data-stu-id="ca71a-105">Many properties are available both from the objects that support them and as columns on tables.</span></span> <span data-ttu-id="ca71a-106">Sempre que possível, recupere essas propriedades por meio da tabela.</span><span class="sxs-lookup"><span data-stu-id="ca71a-106">Whenever possible, retrieve these properties through the table.</span></span>
  
<span data-ttu-id="ca71a-107">Chame [IMAPITable::SetColumns](imapitable-setcolumns.md) para incluir todas as propriedades de que seu cliente precisa e [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar todas as linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="ca71a-107">Call [IMAPITable::SetColumns](imapitable-setcolumns.md) to include all of the properties that your client needs and [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve all of the rows of the table.</span></span> 
  
<span data-ttu-id="ca71a-108">Essas duas chamadas geralmente são suficientes para recuperar informações suficientes para exibição para um usuário e são frequentemente suficientes para qualquer processamento interno necessário, fazendo uma chamada para **OpenEntry** para abrir o objeto desnecessária.</span><span class="sxs-lookup"><span data-stu-id="ca71a-108">These two calls are usually sufficient for retrieving enough information to display to a user, and are frequently sufficient for any necessary internal processing, making a call to **OpenEntry** to open the object unnecessary.</span></span> 
  
<span data-ttu-id="ca71a-109">Há apenas duas exceções:</span><span class="sxs-lookup"><span data-stu-id="ca71a-109">There are only two exceptions:</span></span>
  
- <span data-ttu-id="ca71a-110">Se a propriedade for maior que 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="ca71a-110">If the property is over 255 bytes.</span></span> <span data-ttu-id="ca71a-111">A interface \*\* IMAPITable \*\* pode não retornar o valor inteiro da propriedade, truncando-a em 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="ca71a-111">The \*\* IMAPITable \*\* interface might not return the entire property value, instead truncating it at 255 bytes.</span></span> <span data-ttu-id="ca71a-112">Porém, pense nessa troca.</span><span class="sxs-lookup"><span data-stu-id="ca71a-112">Think about this tradeoff, though.</span></span> <span data-ttu-id="ca71a-113">Se você estiver exibindo esses dados para o usuário, 255 bytes podem ser suficientes para um campo textual, como um comentário.</span><span class="sxs-lookup"><span data-stu-id="ca71a-113">If you are displaying this data to the user, 255 bytes may be enough for a textual field such as a comment.</span></span> 
    
- <span data-ttu-id="ca71a-114">Se você precisar de uma propriedade específica de uma única linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="ca71a-114">If you need a specific property from a single row in a table.</span></span> <span data-ttu-id="ca71a-115">Nesse caso, não é necessário criar uma tabela com propriedades que nunca serão usadas.</span><span class="sxs-lookup"><span data-stu-id="ca71a-115">In this case it is unnecessary to create a table with properties that will never be used.</span></span> <span data-ttu-id="ca71a-116">Na maioria das vezes, você precisará das mesmas propriedades para todas as linhas.</span><span class="sxs-lookup"><span data-stu-id="ca71a-116">Most of the time you will need the same properties for all rows.</span></span>
    

