---
title: Estrutura de fluxo de PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fc20c259f30ded2f96f3bf314e74207bebcac980
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422611"
---
# <a name="packedunicodestring-stream-structure"></a><span data-ttu-id="7fd18-103">Estrutura de fluxo de PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="7fd18-103">PackedUnicodeString Stream Structure</span></span>

  
  
<span data-ttu-id="7fd18-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fd18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fd18-105">A estrutura de fluxo PackedUnicodeString contém uma representação Unicode (UTF-16) de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7fd18-105">The PackedUnicodeString stream structure contains a Unicode (UTF-16) representation of a string.</span></span> <span data-ttu-id="7fd18-106">Essa cadeia de caracteres não é encerrada por um caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="7fd18-106">This string is not terminated by a null character.</span></span> <span data-ttu-id="7fd18-107">Os elementos de dados nesse fluxo são armazenados em ordem de byte little-endian, imediatamente após uns aos outros na ordem listada abaixo.</span><span class="sxs-lookup"><span data-stu-id="7fd18-107">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order listed below.</span></span> <span data-ttu-id="7fd18-108">Os elementos de dados reais existentes dependem do comprimento da cadeia de caracteres na representação UTF-16.</span><span class="sxs-lookup"><span data-stu-id="7fd18-108">The actual data elements that exist depend on the length of the string in UTF-16 representation.</span></span>
  
- <span data-ttu-id="7fd18-109">Para uma cadeia de caracteres cuja representação UTF-16 contenha menos de 255 WCHARs, os elementos de dados são:</span><span class="sxs-lookup"><span data-stu-id="7fd18-109">For a string whose UTF-16 representation contains less than 255 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="7fd18-110">Comprimento: BYTE (1 byte), o comprimento, em número de WCHARs, da representação UTF-16 da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7fd18-110">Length: BYTE (1 byte), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="7fd18-111">Caracteres: uma matriz de WCHAR.</span><span class="sxs-lookup"><span data-stu-id="7fd18-111">Characters: An array of WCHAR.</span></span> <span data-ttu-id="7fd18-112">A contagem dessa matriz é igual ao elemento de dados Length.</span><span class="sxs-lookup"><span data-stu-id="7fd18-112">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="7fd18-113">Os dados na matriz são a representação UTF-16 da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7fd18-113">The data in the array is the UTF-16 representation of the string.</span></span>
    
- <span data-ttu-id="7fd18-114">Para uma cadeia de caracteres cuja representação UTF-16 contém 255 a 65535 WCHARs, os elementos de dados são:</span><span class="sxs-lookup"><span data-stu-id="7fd18-114">For a string whose UTF-16 representation contains 255 to 65535 WCHARs, the data elements are as follows:</span></span>
    
  - <span data-ttu-id="7fd18-115">Prefixo: BYTE (1 byte), o valor de 255 (0xff).</span><span class="sxs-lookup"><span data-stu-id="7fd18-115">Prefix: BYTE (1 byte), the value of 255 (0xff).</span></span>
    
  - <span data-ttu-id="7fd18-116">Comprimento: WORD (2 bytes), o comprimento, em número de WCHARs, da representação UTF-16 da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7fd18-116">Length: WORD (2 bytes), the length, in number of WCHARs, of the UTF-16 representation of the string.</span></span>
    
  - <span data-ttu-id="7fd18-117">Caracteres: uma matriz de WCHAR.</span><span class="sxs-lookup"><span data-stu-id="7fd18-117">Characters: An array of WCHAR.</span></span> <span data-ttu-id="7fd18-118">A contagem dessa matriz é igual ao elemento de dados Length.</span><span class="sxs-lookup"><span data-stu-id="7fd18-118">The count of this array is equal to the Length data element.</span></span> <span data-ttu-id="7fd18-119">Os dados na matriz são a representação UTF-16 da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7fd18-119">The data in the array is the UTF-16 representation of the string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7fd18-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fd18-120">See also</span></span>



[<span data-ttu-id="7fd18-121">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="7fd18-121">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="7fd18-122">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="7fd18-122">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="7fd18-123">Estrutura de Fluxo de FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="7fd18-123">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)

