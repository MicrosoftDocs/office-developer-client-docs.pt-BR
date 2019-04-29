---
title: Estruturas de fluxo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407820"
---
# <a name="stream-structures"></a><span data-ttu-id="333d6-103">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="333d6-103">Stream Structures</span></span>

  
  
<span data-ttu-id="333d6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="333d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="333d6-105">Definições de campos definidos pelo usuário de um item do Microsoft Outlook são armazenadas na propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="333d6-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="333d6-106">O valor dessa propriedade é um fluxo binário que contém definições de campos definidos pelo usuário e configurações de associação de dados para campos internos para o item do Outlook.</span><span class="sxs-lookup"><span data-stu-id="333d6-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="333d6-107">Esta seção fornece informações sobre a estrutura do fluxo binário, divididas nas estruturas de fluxo a seguir.</span><span class="sxs-lookup"><span data-stu-id="333d6-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="333d6-108">Os nomes dessas estruturas de fluxo (por exemplo, PropertyDefinition, FieldDefinition e SkipBlock) e seus elementos de dados não são tecnicamente parte da interface de programação da API de mensagens (MAPI) e são fornecidos aqui somente para documentação objetivos das estruturas de fluxo reais.</span><span class="sxs-lookup"><span data-stu-id="333d6-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="333d6-109">Os desenvolvedores podem rotular essas estruturas de fluxo e elementos de dados em seus aplicativos, conforme eles escolhem.</span><span class="sxs-lookup"><span data-stu-id="333d6-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="333d6-110">Estrutura de fluxo PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="333d6-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="333d6-111">Estrutura de fluxo FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="333d6-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="333d6-112">Estrutura de fluxo SkipBlock</span><span class="sxs-lookup"><span data-stu-id="333d6-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="333d6-113">Estrutura de fluxo FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="333d6-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="333d6-114">Estrutura de fluxo PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="333d6-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="333d6-115">Estrutura de fluxo PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="333d6-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="333d6-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="333d6-116">See also</span></span>



[<span data-ttu-id="333d6-117">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="333d6-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="333d6-118">Adicionar uma definição para um novo campo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="333d6-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="333d6-119">Exemplo de fluxo PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="333d6-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

