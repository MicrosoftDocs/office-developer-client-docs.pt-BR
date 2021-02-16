---
title: Propriedade canônica PidTagUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360736"
---
# <a name="pidtaguserfields-canonical-property"></a><span data-ttu-id="4a96c-103">Propriedade canônica PidTagUserFields</span><span class="sxs-lookup"><span data-stu-id="4a96c-103">PidTagUserFields Canonical Property</span></span>

  
  
<span data-ttu-id="4a96c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a96c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a96c-105">Contém o nome, o tipo de dados e outras informações sobre um campo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4a96c-105">Contains the name, data type, and other information about a user-defined field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a96c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4a96c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a96c-107">PR_USERFIELDS</span><span class="sxs-lookup"><span data-stu-id="4a96c-107">PR_USERFIELDS</span></span>  <br/> |
|<span data-ttu-id="4a96c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4a96c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a96c-109">0x36E3</span><span class="sxs-lookup"><span data-stu-id="4a96c-109">0x36E3</span></span>  <br/> |
|<span data-ttu-id="4a96c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4a96c-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a96c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4a96c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4a96c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4a96c-112">Area:</span></span>  <br/> |<span data-ttu-id="4a96c-113">Pasta MAPI</span><span class="sxs-lookup"><span data-stu-id="4a96c-113">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a96c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a96c-114">Remarks</span></span>

<span data-ttu-id="4a96c-115">Para cada item, o Outlook armazena as definições de todos os campos definidos pelo usuário na propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) do objeto **IMessage** correspondente.</span><span class="sxs-lookup"><span data-stu-id="4a96c-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="4a96c-116">A **propriedade PidLidPropertyDefinitionStream** contém um fluxo binário conhecido como [PropertyDefinition](propertydefinition-stream-structure.md), que contém as definições de campo.</span><span class="sxs-lookup"><span data-stu-id="4a96c-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md), which contains the field definitions.</span></span> <span data-ttu-id="4a96c-117">Para obter mais informações sobre estruturas de fluxo para definições de campo, consulte [Estruturas de fluxo.](stream-structures.md)</span><span class="sxs-lookup"><span data-stu-id="4a96c-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
<span data-ttu-id="4a96c-118">Para cada pasta, o Outlook armazena as definições de todos os campos definidos pelo usuário nessa pasta na propriedade **PidTagUserFields** de uma mensagem associada da classe de mensagem IPC.MS. REN. USERFIELDS - cada pasta presumida de conter não mais de uma mensagem dessa classe em sua tabela de conteúdo associada.</span><span class="sxs-lookup"><span data-stu-id="4a96c-118">For each folder, Outlook stores the definitions of all user-defined fields in that folder in the **PidTagUserFields** property of an associated message of the message class IPC.MS.REN.USERFIELDS - each folder presumed to contain no more than one message of this class in its associated contents table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4a96c-119">O conjunto de campos definidos pelo usuário em uma pasta pode não corresponder necessariamente aos conjuntos de campos definidos pelo usuário em cada um de seus itens.</span><span class="sxs-lookup"><span data-stu-id="4a96c-119">The set of user-defined fields in a folder may not necessarily match the sets of user-defined fields in each of its items.</span></span> 
  
<span data-ttu-id="4a96c-120">O conjunto de campos definidos pelo usuário em uma pasta é exibido em vários lugares na interface do usuário do Outlook, como o Selador de Campos da pasta.</span><span class="sxs-lookup"><span data-stu-id="4a96c-120">The set of user-defined fields in a folder is displayed in various places in the Outlook UI, such as the folder's Field Chooser.</span></span> <span data-ttu-id="4a96c-121">A propriedade **PidTagUserFields** da mensagem contém um fluxo binário, **FolderUserFields**, que contém as definições de campo de pasta.</span><span class="sxs-lookup"><span data-stu-id="4a96c-121">The message's **PidTagUserFields** property contains a binary stream, **FolderUserFields**, which contains the folder field definitions.</span></span> <span data-ttu-id="4a96c-122">Para obter mais informações sobre estruturas de fluxo para definições de campo de pasta, consulte [Estruturas](folder-fields-stream-structures.md) de fluxo de campos de pasta e o exemplo de fluxo [FolderUserFields](folderuserfields-stream-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4a96c-122">For more information about stream structures for folder field definitions, see [Folder Fields Stream Structures](folder-fields-stream-structures.md) and the [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span></span>
  
## <a name="section-heading"></a><span data-ttu-id="4a96c-123">Cabeçalho da seção</span><span class="sxs-lookup"><span data-stu-id="4a96c-123">Section Heading</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a96c-124">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4a96c-124">Protocol specifications</span></span>

<span data-ttu-id="4a96c-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a96c-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a96c-126">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4a96c-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a96c-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="4a96c-127">Header files</span></span>

<span data-ttu-id="4a96c-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a96c-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a96c-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4a96c-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a96c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a96c-130">See also</span></span>



[<span data-ttu-id="4a96c-131">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="4a96c-131">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="4a96c-132">Adicionar uma definição para um novo User-Defined campo</span><span class="sxs-lookup"><span data-stu-id="4a96c-132">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="4a96c-133">Exemplo de fluxo propertyDefinition</span><span class="sxs-lookup"><span data-stu-id="4a96c-133">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="4a96c-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4a96c-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a96c-135">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4a96c-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a96c-136">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4a96c-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a96c-137">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4a96c-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

