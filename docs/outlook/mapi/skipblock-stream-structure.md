---
title: Estrutura de fluxo de SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b7be498473ef86b11006702f85089f0f95bb2e37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580898"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="5c97d-103">Estrutura de fluxo de SkipBlock</span><span class="sxs-lookup"><span data-stu-id="5c97d-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="5c97d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c97d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c97d-105">Uma estrutura de fluxo de SkipBlock é um bloco de dados que começa com um número inteiro que especifica o tamanho da parte restante do bloco.</span><span class="sxs-lookup"><span data-stu-id="5c97d-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="5c97d-106">Essa estrutura stream existe em um stream [FieldDefinition](fielddefinition-stream-structure.md) se a definição de campo está no formato PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="5c97d-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="5c97d-107">A finalidade de uma estrutura de fluxo de SkipBlock depende de seu local relativo em uma série de como estruturas no elemento SkipBlocks dados de um stream FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="5c97d-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="5c97d-108">A série de SkipBlocks deve conter pelo menos uma estrutura SkipBlock que finaliza a série e tem o elemento de dados de tamanho igual a 0.</span><span class="sxs-lookup"><span data-stu-id="5c97d-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="5c97d-109">Se a primeira estrutura não é a estrutura de encerramento (ou seja, o elemento de dados de tamanho é maior que 0), Outlook pressupõe que a primeira estrutura Especifica o nome do campo em Unicode (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="5c97d-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="5c97d-110">Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após a outra na ordem especificada abaixo.</span><span class="sxs-lookup"><span data-stu-id="5c97d-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="5c97d-111">Tamanho: DWORD (4 bytes), o tamanho, em número de bytes, do elemento de dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5c97d-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="5c97d-112">Conteúdo: Uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="5c97d-112">Content: An array of BYTE.</span></span> <span data-ttu-id="5c97d-113">A contagem dessa matriz é igual do elemento de dados de tamanho.</span><span class="sxs-lookup"><span data-stu-id="5c97d-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="5c97d-114">O significado do elemento de dados de conteúdo depende do local da estrutura SkipBlock na série e a versão do Outlook.</span><span class="sxs-lookup"><span data-stu-id="5c97d-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="5c97d-115">Se a primeira estrutura de SkipBlock não for a estrutura de encerramento, o Outlook considera a estrutura de SkipBlock primeira como a estrutura de fluxo de [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) que especifica o nome do campo em Unicode.</span><span class="sxs-lookup"><span data-stu-id="5c97d-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="5c97d-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c97d-116">See also</span></span>



[<span data-ttu-id="5c97d-117">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="5c97d-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="5c97d-118">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="5c97d-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="5c97d-119">Estrutura de fluxo de FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="5c97d-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="5c97d-120">Estrutura de fluxo de FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="5c97d-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

