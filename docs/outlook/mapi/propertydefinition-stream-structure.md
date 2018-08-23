---
title: Estrutura de fluxo de PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b2de22eef455e59b7877524ce998e93a0a708e0c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566653"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="111f4-103">Estrutura de fluxo de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="111f4-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="111f4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="111f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="111f4-105">Uma estrutura de fluxo de PropertyDefinition é uma matriz de estruturas de fluxo de [FieldDefinition](fielddefinition-stream-structure.md) que contêm definições para todos os campos definidos pelo usuário em um item do Microsoft Outlook e configurações de associação de dados para alguns campos internos.</span><span class="sxs-lookup"><span data-stu-id="111f4-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="111f4-106">Programaticamente, você pode manipular a estrutura de fluxo de PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="111f4-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="111f4-107">No entanto, você pode obter resultados semelhantes usando o Designer de formulários do Outlook e, em particular, a caixa de diálogo **Propriedades de** caixa de um controle acoplado a dados.</span><span class="sxs-lookup"><span data-stu-id="111f4-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="111f4-108">Definições de campo em uma estrutura de fluxo de PropertyDefinition podem ser um dos dois formatos: PropDefV1 e PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="111f4-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="111f4-109">O Outlook suporta PropDefV1 e o PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="111f4-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="111f4-110">Todas as definições de campo em uma estrutura de fluxo de PropertyDefinition única devem ser do mesmo formato.</span><span class="sxs-lookup"><span data-stu-id="111f4-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="111f4-111">Para obter mais informações sobre a diferença entre PropDefV1 e PropDefV2, consulte [FieldDefinition Stream estrutura](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="111f4-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="111f4-112">Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após a outra na ordem especificada abaixo.</span><span class="sxs-lookup"><span data-stu-id="111f4-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="111f4-113">Versão: WORD (2 bytes), o formato das definições de campo no PropertyDefinition stream estrutura.</span><span class="sxs-lookup"><span data-stu-id="111f4-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="111f4-114">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="111f4-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="111f4-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="111f4-115">**Value**</span></span>|<span data-ttu-id="111f4-116">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="111f4-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="111f4-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="111f4-117">0x0102</span></span>  <br/> |<span data-ttu-id="111f4-118">Formato é PropDefV1.</span><span class="sxs-lookup"><span data-stu-id="111f4-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="111f4-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="111f4-119">0x0103</span></span>  <br/> |<span data-ttu-id="111f4-120">Formato é PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="111f4-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="111f4-121">FieldDefinitionCount: DWORD (4 bytes), o número de definições de campo neste fluxo.</span><span class="sxs-lookup"><span data-stu-id="111f4-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="111f4-122">É a contagem de elementos de matriz em que o elemento de dados FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="111f4-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="111f4-123">FieldDefinitions: Uma matriz de estruturas de fluxo de FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="111f4-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="111f4-124">A contagem dessa matriz é igual ao elemento FieldDefinitionCount dados.</span><span class="sxs-lookup"><span data-stu-id="111f4-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="111f4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="111f4-125">See also</span></span>

- [<span data-ttu-id="111f4-126">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="111f4-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="111f4-127">Adicionar uma definição de um novo campo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="111f4-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="111f4-128">Exemplo de fluxo de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="111f4-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="111f4-129">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="111f4-129">Stream Structures</span></span>](stream-structures.md)

