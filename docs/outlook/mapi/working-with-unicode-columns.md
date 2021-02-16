---
title: Trabalhando com colunas Unicode
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 76d1afb750dc81b889ca8e5eb3639145c061bfc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408380"
---
# <a name="working-with-unicode-columns"></a><span data-ttu-id="a896f-103">Trabalhando com colunas Unicode</span><span class="sxs-lookup"><span data-stu-id="a896f-103">Working with Unicode Columns</span></span>

  
  
<span data-ttu-id="a896f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a896f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a896f-105">Cadeias de caracteres em tabelas podem ser representadas usando caracteres padrão de 8 bits, que são caracteres do tipo PT_STRING8 ou caracteres Unicode de 16 bits, que são tipos de propriedade PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="a896f-105">Character strings in tables can be represented using standard 8-bit characters, which are property type PT_STRING8, or 16-bit Unicode characters, which are property type PT_UNICODE.</span></span> <span data-ttu-id="a896f-106">Implementadores de tabela são livres para escolher se suas tabelas suportam ou não cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="a896f-106">Table implementers are free to choose whether or not their tables support Unicode strings.</span></span> <span data-ttu-id="a896f-107">Como Unicode adiciona valor para clientes e provedores de serviços estendendo o conjunto de recursos, é recomendável oferecer suporte a Unicode sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="a896f-107">Because Unicode adds value for both clients and service providers by extending the feature set, supporting Unicode wherever possible is recommended.</span></span> 
  
<span data-ttu-id="a896f-108">Muitos métodos de tabela aceitam um sinalizador que determina se os valores de propriedade de cadeia de caracteres devem ou não ser Unicode.</span><span class="sxs-lookup"><span data-stu-id="a896f-108">Many table methods accept a flag that dictates whether or not string property values are expected to be Unicode.</span></span> <span data-ttu-id="a896f-109">Na entrada, especificar o sinalizador MAPI_UNICODE indica ao implementador de tabela que todos os valores de propriedade de cadeia de caracteres passados com a chamada são cadeias de caracteres Unicode e têm tipos de propriedade PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="a896f-109">On input, specifying the MAPI_UNICODE flag indicates to the table implementer that all string property values passed in with the call are Unicode strings and have property types of PT_UNICODE.</span></span> <span data-ttu-id="a896f-110">Na saída, esse sinalizador indica que todos os valores de propriedade de cadeia de caracteres retornados devem ser cadeias de caracteres Unicode, se possível.</span><span class="sxs-lookup"><span data-stu-id="a896f-110">On output, this flag indicates that all returned string property values should be Unicode strings, if possible.</span></span> <span data-ttu-id="a896f-111">Se o sinalizador tem um significado para entrada ou saída depende do método.</span><span class="sxs-lookup"><span data-stu-id="a896f-111">Whether the flag has a meaning for input or output depends on the method.</span></span> <span data-ttu-id="a896f-112">Implementadores de tabela que não suportam Unicode e são passados o sinalizador MAPI_UNICODE retornam o MAPI_E_BAD_CHAR_WIDTH valor.</span><span class="sxs-lookup"><span data-stu-id="a896f-112">Table implementers that do not support Unicode and are passed the MAPI_UNICODE flag return the MAPI_E_BAD_CHAR_WIDTH value.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a896f-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="a896f-113">See also</span></span>



[<span data-ttu-id="a896f-114">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="a896f-114">MAPI Tables</span></span>](mapi-tables.md)

