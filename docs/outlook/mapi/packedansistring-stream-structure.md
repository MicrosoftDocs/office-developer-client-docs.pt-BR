---
title: Estrutura de fluxo de PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404502"
---
# <a name="packedansistring-stream-structure"></a><span data-ttu-id="343dc-103">Estrutura de fluxo de PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="343dc-103">PackedAnsiString Stream Structure</span></span>

  
  
<span data-ttu-id="343dc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="343dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="343dc-105">A estrutura de fluxo PackedAnsiString contém uma representação ANSI de uma cadeia de caracteres, com base na página de código ANSI do computador no qual o Microsoft Outlook está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="343dc-105">The PackedAnsiString stream structure contains an ANSI representation of a string, based on the ANSI code page of the computer on which Microsoft Outlook is running.</span></span> <span data-ttu-id="343dc-106">Essa cadeia de caracteres não é encerrada por um caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="343dc-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="343dc-107">Os elementos de dados nesse fluxo são armazenados em ordem de byte little-endian, imediatamente após uns aos outros na ordem listada abaixo.</span><span class="sxs-lookup"><span data-stu-id="343dc-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="343dc-108">Os elementos de dados reais existentes dependem do comprimento da cadeia de caracteres na representação ANSI.</span><span class="sxs-lookup"><span data-stu-id="343dc-108">The actual data elements that exist depend on the length of the string in ANSI representation.</span></span>
  
- <span data-ttu-id="343dc-109">Para uma cadeia de caracteres cuja representação ANSI contém menos de 255 bytes, os elementos de dados são:</span><span class="sxs-lookup"><span data-stu-id="343dc-109">For a string whose ANSI representation contains less than 255 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="343dc-110">Comprimento: BYTE (1 byte), o comprimento, em número de bytes, da representação ANSI da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="343dc-110">Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="343dc-111">Caracteres: uma matriz de CHAR.</span><span class="sxs-lookup"><span data-stu-id="343dc-111">Characters: An array of CHAR.</span></span> <span data-ttu-id="343dc-112">A contagem dessa matriz é igual ao elemento de dados Length.</span><span class="sxs-lookup"><span data-stu-id="343dc-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="343dc-113">Os dados na matriz são a representação ANSI da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="343dc-113">The data in the array is the ANSI representation of the string.</span></span>
    
- <span data-ttu-id="343dc-114">Para uma cadeia de caracteres cuja representação ANSI contém de 255 a 65535 bytes, os elementos de dados são:</span><span class="sxs-lookup"><span data-stu-id="343dc-114">For a string whose ANSI representation contains 255 to 65535 bytes, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="343dc-115">Prefixo: BYTE (1 byte), o valor de 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="343dc-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="343dc-116">Comprimento: WORD (2 bytes), o comprimento, em número de bytes, da representação ANSI da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="343dc-116">Length: WORD (2 bytes), the length, in number of bytes, of the ANSI representation of the string.</span></span>
    
  - <span data-ttu-id="343dc-117">Caracteres: uma matriz de CHAR.</span><span class="sxs-lookup"><span data-stu-id="343dc-117">Characters: An array of CHAR.</span></span> <span data-ttu-id="343dc-118">A contagem dessa matriz é igual ao elemento de dados Length.</span><span class="sxs-lookup"><span data-stu-id="343dc-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="343dc-119">Os dados na matriz são a representação ANSI da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="343dc-119">The data in the array is the ANSI representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="343dc-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="343dc-120">See also</span></span>



[<span data-ttu-id="343dc-121">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="343dc-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="343dc-122">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="343dc-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="343dc-123">Estrutura de Fluxo de FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="343dc-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

