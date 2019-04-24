---
title: Estrutura de fluxo SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5a3367a15374234658fd9d10f3c2a5f3a191c80e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282667"
---
# <a name="skipblock-stream-structure"></a><span data-ttu-id="414cf-103">Estrutura de fluxo SkipBlock</span><span class="sxs-lookup"><span data-stu-id="414cf-103">SkipBlock Stream Structure</span></span>

  
  
<span data-ttu-id="414cf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="414cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="414cf-105">Uma estrutura de fluxo SkipBlock é um bloco de dados que começa com um inteiro que especifica o comprimento da parte restante do bloco.</span><span class="sxs-lookup"><span data-stu-id="414cf-105">A SkipBlock stream structure is a block of data that starts with an integer that specifies the length of the remaining part of the block.</span></span> <span data-ttu-id="414cf-106">Essa estrutura de fluxo existe em um fluxo de [FieldDefinition](fielddefinition-stream-structure.md) se a definição de campo estiver no formato PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="414cf-106">This stream structure exists in a [FieldDefinition](fielddefinition-stream-structure.md) stream if the field definition is in PropDefV2 format.</span></span> 
  
<span data-ttu-id="414cf-107">A finalidade de uma estrutura de fluxo do SkipBlock depende de seu local relativo em uma série de estruturas semelhantes no elemento de dados SkipBlocks de um fluxo de FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="414cf-107">The purpose of a SkipBlock stream structure depends on its relative location in a series of like structures in the SkipBlocks data element of a FieldDefinition stream.</span></span> <span data-ttu-id="414cf-108">A série SkipBlocks deve conter pelo menos uma estrutura SkipBlock que termine a série e tenha o elemento de dados de tamanho igual a 0.</span><span class="sxs-lookup"><span data-stu-id="414cf-108">The SkipBlocks series should contain at least one SkipBlock structure that terminates the series and has the Size data element equal to 0.</span></span> <span data-ttu-id="414cf-109">Se a primeira estrutura não for a estrutura de terminação (ou seja, o elemento de dados size for maior que 0), o Outlook presumirá que a primeira estrutura especifica o nome do campo em Unicode (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="414cf-109">If the first structure is not the terminating structure (that is, the Size data element is greater than 0), Outlook assumes the first structure specifies the field name in Unicode (UTF-16).</span></span>
  
<span data-ttu-id="414cf-110">Os elementos de dados neste fluxo são armazenados em uma ordem de byte little-endian, imediatamente após o outro na ordem especificada abaixo.</span><span class="sxs-lookup"><span data-stu-id="414cf-110">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="414cf-111">Tamanho: DWORD (4 bytes), o tamanho, em número de bytes, do elemento de dados de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="414cf-111">Size: DWORD (4 bytes), the size, in number of bytes, of the Content data element.</span></span>
    
- <span data-ttu-id="414cf-112">Conteúdo: uma matriz de BYTE.</span><span class="sxs-lookup"><span data-stu-id="414cf-112">Content: An array of BYTE.</span></span> <span data-ttu-id="414cf-113">A contagem dessa matriz é igual ao elemento de dados de tamanho.</span><span class="sxs-lookup"><span data-stu-id="414cf-113">The count of this array is equal to the Size data element.</span></span> <span data-ttu-id="414cf-114">O significado do elemento de dados de conteúdo depende do local da estrutura SkipBlock da série e da versão do Outlook.</span><span class="sxs-lookup"><span data-stu-id="414cf-114">The meaning of the Content data element depends on the location of the SkipBlock structure in the series and the version of Outlook.</span></span> <span data-ttu-id="414cf-115">Se a primeira estrutura SkipBlock não for a estrutura de terminação, o Outlook considerará a primeira estrutura SkipBlock como a estrutura de fluxo de [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) que especifica o nome do campo em Unicode.</span><span class="sxs-lookup"><span data-stu-id="414cf-115">If the first SkipBlock structure is not the terminating structure, Outlook considers the first SkipBlock structure as the [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) stream structure that specifies the field name in Unicode.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="414cf-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="414cf-116">See also</span></span>



[<span data-ttu-id="414cf-117">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="414cf-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="414cf-118">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="414cf-118">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="414cf-119">Estrutura de fluxo FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="414cf-119">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="414cf-120">Estrutura de fluxo FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="414cf-120">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)

