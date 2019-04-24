---
title: Adicionar uma definição de um novo campo definido pelo usuário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299066"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="f6b63-103">Adicionar uma definição de um novo campo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="f6b63-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="f6b63-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6b63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6b63-105">Quando você adiciona um campo definido pelo usuário a um item do Microsoft Outlook, você adiciona uma definição de campo à estrutura de fluxo [PropertyDefinition](propertydefinition-stream-structure.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="f6b63-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="f6b63-106">Use o procedimento a seguir para adicionar uma nova definição de campo a uma estrutura de fluxo do PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f6b63-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="f6b63-107">Para adicionar uma definição para um novo campo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="f6b63-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="f6b63-108">Copie as definições de campo existentes da estrutura de fluxo do PropertyDefinition para uma nova matriz de definições de campos.</span><span class="sxs-lookup"><span data-stu-id="f6b63-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="f6b63-109">Se quaisquer definições de campo existentes estiverem no formato PropDefV1, converta-as no formato PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="f6b63-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="f6b63-110">Para obter mais informações sobre formatos de definição de campos, consulte [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) e [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="f6b63-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="f6b63-111">Criar uma definição do novo campo definido pelo usuário no formato PropDefV2 e adicioná-lo à matriz.</span><span class="sxs-lookup"><span data-stu-id="f6b63-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="f6b63-112">Defina o elemento Version da estrutura de fluxo PropertyDefinition como 0x0103, se o elemento Version não tiver sido definido para esse valor.</span><span class="sxs-lookup"><span data-stu-id="f6b63-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="f6b63-113">Incrementa o elemento FieldDefinitionCount em 1.</span><span class="sxs-lookup"><span data-stu-id="f6b63-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="f6b63-114">Armazene a matriz como o valor do elemento FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="f6b63-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6b63-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6b63-115">See also</span></span>

- [<span data-ttu-id="f6b63-116">Estrutura de fluxo PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="f6b63-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

