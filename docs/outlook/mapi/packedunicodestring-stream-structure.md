---
title: Estrutura de fluxo de PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2b4dcdcb50fb04410ed93940b46ea7a0d74fff41
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768202"
---
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="e4bf6-103">Estrutura de fluxo de PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="e4bf6-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="e4bf6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4bf6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4bf6-105">A estrutura de fluxo de PackedUnicodeString contém uma representação Unicode (UTF-16) de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e4bf6-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="e4bf6-106">Esta cadeia de caracteres não será terminada por um caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="e4bf6-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="e4bf6-107">Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após a outra na ordem listada abaixo.</span><span class="sxs-lookup"><span data-stu-id="e4bf6-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="e4bf6-108">Os elementos de dados reais que existem dependem do comprimento da cadeia de caracteres na representação UTF-16.</span><span class="sxs-lookup"><span data-stu-id="e4bf6-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="e4bf6-109">Para uma cadeia de caracteres cuja representação UTF-16 contém menor do que 255 WCHARs, os elementos de dados são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="e4bf6-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="e4bf6-110">Duração: BYTE (1 byte), o comprimento, em número de WCHARs, da codificação UTF-16 representação da sequência de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e4bf6-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="e4bf6-111">Caracteres: Uma matriz de WCHAR.</span><span class="sxs-lookup"><span data-stu-id="e4bf6-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="e4bf6-112">A contagem dessa matriz é igual do elemento de dados de comprimento.</span><span class="sxs-lookup"><span data-stu-id="e4bf6-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="e4bf6-113">Os dados na matriz são a representação UTF-16 da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e4bf6-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="e4bf6-114">Para uma cadeia de caracteres cuja representação UTF-16 contém WCHARs 255 e 65535, os elementos de dados são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="e4bf6-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="e4bf6-115">Prefixo: BYTE (1 byte), o valor de 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="e4bf6-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="e4bf6-116">Duração: WORD (2 bytes), o comprimento, em número de WCHARs, da codificação UTF-16 representação da sequência de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e4bf6-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="e4bf6-117">Caracteres: Uma matriz de WCHAR.</span><span class="sxs-lookup"><span data-stu-id="e4bf6-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="e4bf6-118">A contagem dessa matriz é igual do elemento de dados de comprimento.</span><span class="sxs-lookup"><span data-stu-id="e4bf6-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="e4bf6-119">Os dados na matriz são a representação UTF-16 da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e4bf6-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e4bf6-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4bf6-120">See also</span></span>



[<span data-ttu-id="e4bf6-121">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="e4bf6-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="e4bf6-122">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="e4bf6-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="e4bf6-123">Estrutura de fluxo de FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="e4bf6-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
