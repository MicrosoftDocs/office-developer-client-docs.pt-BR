---
title: Estruturas de fluxo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6ec44fe0dbf8e63b7bbc58da1ba6e20f8ff59d3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770513"
---
# <a name="stream-structures"></a><span data-ttu-id="4faab-103">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="4faab-103">Stream Structures</span></span>

  
  
<span data-ttu-id="4faab-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4faab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4faab-105">Definições de campos definida pelo usuário de um item do Microsoft Outlook são armazenadas na propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="4faab-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="4faab-106">O valor dessa propriedade é um fluxo binário que contém definições de campos definidos pelo usuário e configurações de associação de dados para campos internos do item do Outlook.</span><span class="sxs-lookup"><span data-stu-id="4faab-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="4faab-107">Esta seção fornece informações sobre a estrutura do fluxo binário, decomposta nas seguintes estruturas stream.</span><span class="sxs-lookup"><span data-stu-id="4faab-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4faab-108">Os nomes dessas estruturas stream (por exemplo, PropertyDefinition, FieldDefinition e SkipBlock) e seus elementos de dados não são tecnicamente fazem parte da interface de programação de API do MAPI (Messaging) e são oferecidos apenas para documentação fins as estruturas de fluxo real.</span><span class="sxs-lookup"><span data-stu-id="4faab-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="4faab-109">Desenvolvedores podem rotular esses elementos de estruturas e os dados de fluxo em seus aplicativos de forma que preferirem.</span><span class="sxs-lookup"><span data-stu-id="4faab-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="4faab-110">Estrutura de fluxo de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="4faab-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="4faab-111">Estrutura de fluxo de FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="4faab-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="4faab-112">Estrutura de fluxo de SkipBlock</span><span class="sxs-lookup"><span data-stu-id="4faab-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="4faab-113">Estrutura de fluxo de FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="4faab-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="4faab-114">Estrutura de fluxo de PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="4faab-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="4faab-115">Estrutura de fluxo de PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="4faab-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="4faab-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="4faab-116">See also</span></span>



[<span data-ttu-id="4faab-117">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="4faab-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="4faab-118">Adicionar uma definição de um novo campo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="4faab-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="4faab-119">Exemplo de fluxo de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="4faab-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

