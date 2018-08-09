---
title: Estrutura de fluxo de PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5494558db65e19891848264c170ba85a55c5df71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768199"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="cd555-103">Estrutura de fluxo de PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="cd555-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="cd555-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cd555-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cd555-105">A estrutura de fluxo de PackedAnsiString contém uma representação de ANSI de uma cadeia de caracteres, com base na página de código ANSI do computador no qual está executando o Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="cd555-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="cd555-106">Esta cadeia de caracteres não será terminada por um caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="cd555-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="cd555-107">Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após a outra na ordem listada abaixo.</span><span class="sxs-lookup"><span data-stu-id="cd555-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="cd555-108">Os elementos de dados reais que existem dependem do comprimento da cadeia de caracteres na representação ANSI.</span><span class="sxs-lookup"><span data-stu-id="cd555-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="cd555-109">Para uma cadeia de caracteres cuja representação ANSI contém menor do que 255 bytes, os elementos de dados são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="cd555-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="cd555-110">Duração: BYTE (1 byte), o comprimento, em número de bytes, da representação da sequência de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="cd555-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="cd555-111">Caracteres: Uma matriz de CHAR.</span><span class="sxs-lookup"><span data-stu-id="cd555-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="cd555-112">A contagem dessa matriz é igual do elemento de dados de comprimento.</span><span class="sxs-lookup"><span data-stu-id="cd555-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="cd555-113">Os dados na matriz são a representação de ANSI da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd555-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="cd555-114">Para uma cadeia de caracteres cuja representação ANSI contém 255 a 65.535 bytes, os elementos de dados são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="cd555-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="cd555-115">Prefixo: BYTE (1 byte), o valor de 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="cd555-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="cd555-116">Duração: WORD (2 bytes), o comprimento, em número de bytes, da representação da sequência de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="cd555-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="cd555-117">Caracteres: Uma matriz de CHAR.</span><span class="sxs-lookup"><span data-stu-id="cd555-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="cd555-118">A contagem dessa matriz é igual do elemento de dados de comprimento.</span><span class="sxs-lookup"><span data-stu-id="cd555-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="cd555-119">Os dados na matriz são a representação de ANSI da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd555-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd555-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd555-120">See also</span></span>



[<span data-ttu-id="cd555-121">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="cd555-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="cd555-122">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="cd555-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="cd555-123">Estrutura de fluxo de FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="cd555-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

