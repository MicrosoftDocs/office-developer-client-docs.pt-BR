---
title: Estrutura de fluxo PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ab677a06-6d7d-47e7-99ea-535b0b24389a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 479339762867aa778bc8bc8baa1f21f6bc34b441
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438586"
---
# <a name="propertydefinition-stream-structure"></a><span data-ttu-id="cae1b-103">Estrutura de fluxo PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="cae1b-103">PropertyDefinition stream structure</span></span>

<span data-ttu-id="cae1b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cae1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cae1b-105">Uma estrutura de fluxo PropertyDefinition é uma matriz de estruturas de fluxo [FieldDefinition](fielddefinition-stream-structure.md) que contêm definições para todos os campos definidos pelo usuário em um item do Microsoft Outlook e configurações de vinculação de dados para alguns campos integrados.</span><span class="sxs-lookup"><span data-stu-id="cae1b-105">A PropertyDefinition stream structure is an array of [FieldDefinition](fielddefinition-stream-structure.md) stream structures that contain definitions for all user-defined fields in a Microsoft Outlook item, and data-binding settings for some built-in fields.</span></span> 
  
<span data-ttu-id="cae1b-106">Você pode manipular programaticamente a estrutura de fluxo PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="cae1b-106">You can programmatically manipulate the PropertyDefinition stream structure.</span></span> <span data-ttu-id="cae1b-107">No entanto, você pode obter resultados semelhantes usando o  Designer de Formulários do Outlook e, em particular, a caixa de diálogo Propriedades para um controle vinculado a dados.</span><span class="sxs-lookup"><span data-stu-id="cae1b-107">However, you can achieve similar results by using the Outlook Forms Designer and, in particular, the **Properties** dialog box for a data-bound control.</span></span> 
  
<span data-ttu-id="cae1b-108">As definições de campo em uma estrutura de fluxo PropertyDefinition podem ser um dos dois formatos: PropDefV1 e PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="cae1b-108">Field definitions in a PropertyDefinition stream structure can be one of two formats: PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="cae1b-109">O Outlook dá suporte a PropDefV1 e PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="cae1b-109">Outlook supports both PropDefV1 and PropDefV2.</span></span> <span data-ttu-id="cae1b-110">Todas as definições de campo em uma única estrutura de fluxo PropertyDefinition devem ter o mesmo formato.</span><span class="sxs-lookup"><span data-stu-id="cae1b-110">All field definitions in a single PropertyDefinition stream structure must be of the same format.</span></span> <span data-ttu-id="cae1b-111">Para obter mais informações sobre como PropDefV1 e PropDefV2 diferem, consulte [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="cae1b-111">For more information about how PropDefV1 and PropDefV2 differ, see [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
  
<span data-ttu-id="cae1b-112">Os elementos de dados nesse fluxo são armazenados em ordem de byte little-endian, imediatamente após uns aos outros na ordem especificada abaixo.</span><span class="sxs-lookup"><span data-stu-id="cae1b-112">Data elements in this stream are stored in little-endian byte order, immediately following each other in the order specified below.</span></span>
  
- <span data-ttu-id="cae1b-113">Versão: WORD (2 bytes), o formato das definições de campo na estrutura de fluxo PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="cae1b-113">Version: WORD (2 bytes), the format of the field definitions in the PropertyDefinition stream structure.</span></span> <span data-ttu-id="cae1b-114">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="cae1b-114">The following table shows the possible values.</span></span>
    
    |<span data-ttu-id="cae1b-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cae1b-115">**Value**</span></span>|<span data-ttu-id="cae1b-116">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cae1b-116">**Description**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="cae1b-117">0x0102</span><span class="sxs-lookup"><span data-stu-id="cae1b-117">0x0102</span></span>  <br/> |<span data-ttu-id="cae1b-118">O formato é PropDefV1.</span><span class="sxs-lookup"><span data-stu-id="cae1b-118">Format is PropDefV1.</span></span>  <br/> |
    |<span data-ttu-id="cae1b-119">0x0103</span><span class="sxs-lookup"><span data-stu-id="cae1b-119">0x0103</span></span>  <br/> |<span data-ttu-id="cae1b-120">O formato é PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="cae1b-120">Format is PropDefV2.</span></span>  <br/> |
   
- <span data-ttu-id="cae1b-121">FieldDefinitionCount: DWORD (4 bytes), o número de definições de campo neste fluxo.</span><span class="sxs-lookup"><span data-stu-id="cae1b-121">FieldDefinitionCount: DWORD (4 bytes), the number of field definitions in this stream.</span></span> <span data-ttu-id="cae1b-122">Esta é a contagem de elementos de matriz no elemento de dados FieldDefinitions.</span><span class="sxs-lookup"><span data-stu-id="cae1b-122">This is the count of array elements in the FieldDefinitions data element.</span></span>
    
- <span data-ttu-id="cae1b-123">FieldDefinitions: uma matriz de estruturas de fluxo FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="cae1b-123">FieldDefinitions: An array of FieldDefinition stream structures.</span></span> <span data-ttu-id="cae1b-124">A contagem dessa matriz é igual ao elemento de dados FieldDefinitionCount.</span><span class="sxs-lookup"><span data-stu-id="cae1b-124">The count of this array is equal to the FieldDefinitionCount data element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cae1b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="cae1b-125">See also</span></span>

- [<span data-ttu-id="cae1b-126">Campos e itens do Outlook</span><span class="sxs-lookup"><span data-stu-id="cae1b-126">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="cae1b-127">Adicionar uma definição para um novo User-Defined campo</span><span class="sxs-lookup"><span data-stu-id="cae1b-127">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
- [<span data-ttu-id="cae1b-128">Exemplo de fluxo propertyDefinition</span><span class="sxs-lookup"><span data-stu-id="cae1b-128">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
- [<span data-ttu-id="cae1b-129">Estruturas de fluxo</span><span class="sxs-lookup"><span data-stu-id="cae1b-129">Stream Structures</span></span>](stream-structures.md)

