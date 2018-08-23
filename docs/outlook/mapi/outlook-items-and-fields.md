---
title: Campos e itens do Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: caa231842c5fd51deb80144f12fdf53e51ccc980
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582872"
---
# <a name="outlook-items-and-fields"></a><span data-ttu-id="753ac-103">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="753ac-103">Outlook Items and Fields</span></span>

  
  
<span data-ttu-id="753ac-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="753ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="753ac-105">Microsoft Outlook fornece os tipos de itens que são especializados para sua funcionalidade (por exemplo, itens de email, compromissos, contatos, tarefas e anotações).</span><span class="sxs-lookup"><span data-stu-id="753ac-105">Microsoft Outlook provides item types that are specialized for their functionality (for example, mail items, appointments, contacts, tasks, and notes).</span></span> <span data-ttu-id="753ac-106">Outlook fornece campos padrão para cada tipo de item, normalmente conhecido como campos internos.</span><span class="sxs-lookup"><span data-stu-id="753ac-106">Outlook provides standard fields for each type of item, commonly referred to as built-in fields.</span></span> <span data-ttu-id="753ac-107">Outlook também permite aos usuários criar campos personalizados, comumente conhecidos como campos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="753ac-107">Outlook also allows users to create custom fields, commonly referred to as user-defined fields.</span></span> <span data-ttu-id="753ac-108">Cada campo é associado um tipo de dados e um valor.</span><span class="sxs-lookup"><span data-stu-id="753ac-108">Each field is associated with a data type and a value.</span></span> <span data-ttu-id="753ac-109">Exemplos dos tipos de dados são **moeda**, **Data/hora**, **duração**, **Integer**, **palavras-chave**e **texto**.</span><span class="sxs-lookup"><span data-stu-id="753ac-109">Examples of data types are **Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords**, and **Text**.</span></span> <span data-ttu-id="753ac-110">Os usuários podem definir campos personalizados usando o Designer de formulários do Outlook.</span><span class="sxs-lookup"><span data-stu-id="753ac-110">Users can define custom fields by using the Forms Designer in Outlook.</span></span>
  
<span data-ttu-id="753ac-111">No nível de programação, cada item é representado por um objeto [IMessage](imessageimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="753ac-111">At the programmability level, each item is represented by an [IMessage](imessageimapiprop.md) object.</span></span> <span data-ttu-id="753ac-112">Cada campo definido pelo usuário é associado uma definição de campo e um valor.</span><span class="sxs-lookup"><span data-stu-id="753ac-112">Each user-defined field is associated with a field definition and a value.</span></span> 
  
### <a name="field-definition"></a><span data-ttu-id="753ac-113">Definição de campo</span><span class="sxs-lookup"><span data-stu-id="753ac-113">Field Definition</span></span>

<span data-ttu-id="753ac-114">Uma definição de campo inclui o nome, tipo de dados e outras informações sobre o campo.</span><span class="sxs-lookup"><span data-stu-id="753ac-114">A field definition includes the name, data type, and other information about the field.</span></span> <span data-ttu-id="753ac-115">Para cada item, o Outlook armazena as definições de todos os campos definidos pelo usuário na propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) do objeto **IMessage** correspondente.</span><span class="sxs-lookup"><span data-stu-id="753ac-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="753ac-116">A propriedade **PidLidPropertyDefinitionStream** contém um fluxo binário conhecido como [PropertyDefinition](propertydefinition-stream-structure.md) que contém as definições de campo.</span><span class="sxs-lookup"><span data-stu-id="753ac-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md) that contains the field definitions.</span></span> <span data-ttu-id="753ac-117">Para obter mais informações sobre as estruturas de fluxo de definições de campo, consulte [Estruturas de Stream](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="753ac-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
### <a name="field-value"></a><span data-ttu-id="753ac-118">Valor do campo</span><span class="sxs-lookup"><span data-stu-id="753ac-118">Field Value</span></span>

<span data-ttu-id="753ac-119">Cada campo definido pelo usuário de um item tem um valor que é armazenado em uma propriedade denominada correspondente.</span><span class="sxs-lookup"><span data-stu-id="753ac-119">Each user-defined field of an item has a value that is stored in a corresponding named property.</span></span> <span data-ttu-id="753ac-120">Que a propriedade nomeada está no conjunto de propriedades PS_PUBLIC_STRINGS e tem uma cadeia de caracteres Unicode como o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="753ac-120">That named property is in the PS_PUBLIC_STRINGS property set, and has a Unicode character string as the property name.</span></span> <span data-ttu-id="753ac-121">O tipo de dados da propriedade corresponde ao tipo de campo.</span><span class="sxs-lookup"><span data-stu-id="753ac-121">The data type of the property corresponds to the type of the field.</span></span> <span data-ttu-id="753ac-122">Se a propriedade não estiver presente no objeto **IMessage** , o Outlook pressupõe um valor razoável padrão para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="753ac-122">If the property is not present in the **IMessage** object, Outlook assumes a reasonable default value for the property.</span></span> <span data-ttu-id="753ac-123">Por exemplo, para um tipo de cadeia de caracteres, Outlook assume uma cadeia de caracteres vazia se a propriedade não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="753ac-123">For example, for a string type, Outlook assumes an empty string if the property is not present.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="753ac-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="753ac-124">See also</span></span>



[<span data-ttu-id="753ac-125">Adicionar uma definição de um novo campo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="753ac-125">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="753ac-126">Exemplo de fluxo de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="753ac-126">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="753ac-127">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="753ac-127">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="753ac-128">Estrutura de fluxo de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="753ac-128">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
  
[<span data-ttu-id="753ac-129">Estrutura de fluxo de FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="753ac-129">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="753ac-130">Estrutura de fluxo de SkipBlock</span><span class="sxs-lookup"><span data-stu-id="753ac-130">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
  
[<span data-ttu-id="753ac-131">Estrutura de fluxo de FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="753ac-131">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
  
[<span data-ttu-id="753ac-132">Estrutura de fluxo de PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="753ac-132">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
  
[<span data-ttu-id="753ac-133">Estrutura de fluxo de PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="753ac-133">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

