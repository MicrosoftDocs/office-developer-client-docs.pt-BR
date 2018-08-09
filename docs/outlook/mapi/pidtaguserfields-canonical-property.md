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
ms.openlocfilehash: 5abfd9c98c5a83ca45792f094d0c9573b8affb85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770145"
---
# <a name="pidtaguserfields-canonical-property"></a><span data-ttu-id="2ed6a-103">Propriedade canônica PidTagUserFields</span><span class="sxs-lookup"><span data-stu-id="2ed6a-103">PidTagUserFields Canonical Property</span></span>

  
  
<span data-ttu-id="2ed6a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2ed6a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2ed6a-105">Contém o nome, tipo de dados e outras informações sobre um campo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2ed6a-105">Contains the name, data type, and other information about a user-defined field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ed6a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2ed6a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ed6a-107">PR_USERFIELDS</span><span class="sxs-lookup"><span data-stu-id="2ed6a-107">PR_USERFIELDS</span></span>  <br/> |
|<span data-ttu-id="2ed6a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2ed6a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ed6a-109">0x36E3</span><span class="sxs-lookup"><span data-stu-id="2ed6a-109">0x36E3</span></span>  <br/> |
|<span data-ttu-id="2ed6a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2ed6a-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ed6a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2ed6a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2ed6a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="2ed6a-112">Area:</span></span>  <br/> |<span data-ttu-id="2ed6a-113">Pasta MAPI</span><span class="sxs-lookup"><span data-stu-id="2ed6a-113">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ed6a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ed6a-114">Remarks</span></span>

<span data-ttu-id="2ed6a-115">Para cada item, o Outlook armazena as definições de todos os campos definidos pelo usuário na propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) do objeto **IMessage** correspondente.</span><span class="sxs-lookup"><span data-stu-id="2ed6a-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="2ed6a-116">A propriedade **PidLidPropertyDefinitionStream** contém um fluxo binário conhecido como [PropertyDefinition](propertydefinition-stream-structure.md), que contém as definições de campo.</span><span class="sxs-lookup"><span data-stu-id="2ed6a-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md), which contains the field definitions.</span></span> <span data-ttu-id="2ed6a-117">Para obter mais informações sobre as estruturas de fluxo de definições de campo, consulte [Estruturas de Stream](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="2ed6a-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
<span data-ttu-id="2ed6a-118">Para cada pasta, o Outlook armazena as definições de todos os campos definidos pelo usuário nessa pasta na propriedade **PidTagUserFields** de uma mensagem associada da classe de mensagem, IPC.MS. REN. CAMPOS - cada pasta provável que contenha não mais de uma mensagem desta classe na sua tabela de conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="2ed6a-118">For each folder, Outlook stores the definitions of all user-defined fields in that folder in the **PidTagUserFields** property of an associated message of the message class IPC.MS.REN.USERFIELDS - each folder presumed to contain no more than one message of this class in its associated contents table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2ed6a-119">O conjunto de campos definido pelo usuário em uma pasta pode não necessariamente corresponder os conjuntos de campos definidos pelo usuário em cada um dos seus itens.</span><span class="sxs-lookup"><span data-stu-id="2ed6a-119">The set of user-defined fields in a folder may not necessarily match the sets of user-defined fields in each of its items.</span></span> 
  
<span data-ttu-id="2ed6a-120">O conjunto de campos definido pelo usuário em uma pasta é exibido em vários locais da UI do Outlook, como o seletor de campos da pasta.</span><span class="sxs-lookup"><span data-stu-id="2ed6a-120">The set of user-defined fields in a folder is displayed in various places in the Outlook UI, such as the folder's Field Chooser.</span></span> <span data-ttu-id="2ed6a-121">Propriedade **PidTagUserFields** da mensagem contém um fluxo binário, **FolderUserFields**, que contém as definições de campo da pasta.</span><span class="sxs-lookup"><span data-stu-id="2ed6a-121">The message's **PidTagUserFields** property contains a binary stream, **FolderUserFields**, which contains the folder field definitions.</span></span> <span data-ttu-id="2ed6a-122">Para obter mais informações sobre as estruturas de fluxo de definições de campo de pasta, consulte [Pasta estruturas de fluxo de campos](folder-fields-stream-structures.md) e a [Amostra de fluxo de FolderUserFields](folderuserfields-stream-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2ed6a-122">For more information about stream structures for folder field definitions, see [Folder Fields Stream Structures](folder-fields-stream-structures.md) and the [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span></span>
  
## <a name="section-heading"></a><span data-ttu-id="2ed6a-123">Cabeçalho da seção</span><span class="sxs-lookup"><span data-stu-id="2ed6a-123">Section Heading</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2ed6a-124">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2ed6a-124">Protocol specifications</span></span>

<span data-ttu-id="2ed6a-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2ed6a-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2ed6a-126">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="2ed6a-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2ed6a-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2ed6a-127">Header files</span></span>

<span data-ttu-id="2ed6a-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ed6a-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ed6a-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2ed6a-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ed6a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ed6a-130">See also</span></span>



[<span data-ttu-id="2ed6a-131">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="2ed6a-131">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="2ed6a-132">Adicionar uma definição de um novo campo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="2ed6a-132">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="2ed6a-133">Exemplo de fluxo de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="2ed6a-133">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="2ed6a-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2ed6a-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ed6a-135">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="2ed6a-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ed6a-136">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2ed6a-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ed6a-137">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2ed6a-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

