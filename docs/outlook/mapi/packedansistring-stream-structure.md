---
title: Estrutura de fluxo de PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4e919270efb196cda845581830cc4a918012b385
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578973"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="c961e-103">Estrutura de fluxo de PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="c961e-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="c961e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c961e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c961e-105">A estrutura de fluxo de PackedAnsiString contém uma representação de ANSI de uma cadeia de caracteres, com base na página de código ANSI do computador no qual está executando o Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="c961e-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="c961e-106">Esta cadeia de caracteres não será terminada por um caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="c961e-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="c961e-107">Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após a outra na ordem listada abaixo.</span><span class="sxs-lookup"><span data-stu-id="c961e-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="c961e-108">Os elementos de dados reais que existem dependem do comprimento da cadeia de caracteres na representação ANSI.</span><span class="sxs-lookup"><span data-stu-id="c961e-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="c961e-109">Para uma cadeia de caracteres cuja representação ANSI contém menor do que 255 bytes, os elementos de dados são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="c961e-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="c961e-110">Duração: BYTE (1 byte), o comprimento, em número de bytes, da representação da sequência de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="c961e-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="c961e-111">Caracteres: Uma matriz de CHAR.</span><span class="sxs-lookup"><span data-stu-id="c961e-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="c961e-112">A contagem dessa matriz é igual do elemento de dados de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c961e-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="c961e-113">Os dados na matriz são a representação de ANSI da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c961e-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="c961e-114">Para uma cadeia de caracteres cuja representação ANSI contém 255 a 65.535 bytes, os elementos de dados são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="c961e-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="c961e-115">Prefixo: BYTE (1 byte), o valor de 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="c961e-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="c961e-116">Duração: WORD (2 bytes), o comprimento, em número de bytes, da representação da sequência de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="c961e-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="c961e-117">Caracteres: Uma matriz de CHAR.</span><span class="sxs-lookup"><span data-stu-id="c961e-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="c961e-118">A contagem dessa matriz é igual do elemento de dados de comprimento.</span><span class="sxs-lookup"><span data-stu-id="c961e-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="c961e-119">Os dados na matriz são a representação de ANSI da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c961e-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c961e-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c961e-120">See also</span></span>



[<span data-ttu-id="c961e-121">Campos e itens do outlook</span><span class="sxs-lookup"><span data-stu-id="c961e-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="c961e-122">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="c961e-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="c961e-123">Estrutura de fluxo de FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="c961e-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

