---
title: Adicione uma definição para um novo campo definido pelo usuário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 26c329323eebff6cfdf4f4be4dffe9a62f8745e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766703"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="9b6b8-103">Adicione uma definição para um novo campo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="9b6b8-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="9b6b8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9b6b8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9b6b8-105">Quando você adiciona um campo definido pelo usuário a um item do Microsoft Outlook, você adicionar uma definição de campo na estrutura do stream [PropertyDefinition](propertydefinition-stream-structure.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="9b6b8-106">Use o procedimento a seguir para adicionar uma nova definição de campo para uma estrutura de fluxo de PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="9b6b8-107">Para adicionar uma definição para um novo campo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="9b6b8-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="9b6b8-108">Copie as definições de campo existentes da estrutura PropertyDefinition stream para uma nova matriz de definições de campo.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="9b6b8-109">Se quaisquer definições de campo existente no formato PropDefV1, convertê-los para o formato de PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="9b6b8-110">Para obter mais informações sobre formatos de definição de campo, consulte [PropertyDefinition Stream](propertydefinition-stream-structure.md) e [Estrutura do fluxo de FieldDefinition](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="9b6b8-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="9b6b8-111">Criar uma definição do novo campo definido pelo usuário no formato PropDefV2 e adicioná-lo à matriz.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="9b6b8-112">Defina o elemento de versão da estrutura PropertyDefinition stream como 0x0103, se o elemento de versão não tiver sido definido para esse valor.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="9b6b8-113">Aumentam o elemento FieldDefinitionCount em 1.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="9b6b8-114">Armazene a matriz como o valor do elemento FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="9b6b8-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b6b8-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b6b8-115">See also</span></span>

- [<span data-ttu-id="9b6b8-116">Estrutura de fluxo de PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="9b6b8-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

