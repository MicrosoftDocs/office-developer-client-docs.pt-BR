---
title: Elemento de problemas (Validation_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Contém todos os elementos de problema para o documento.
ms.openlocfilehash: 9205bf014c81aa699b8bc4a2a7412c5ce59c5fd0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772114"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="352ab-103">Elemento de problemas (Validation_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="352ab-103">Issues element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="352ab-104">Contém todos os elementos de problema para o documento.</span><span class="sxs-lookup"><span data-stu-id="352ab-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="352ab-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="352ab-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="352ab-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="352ab-106">**Element type**</span></span> <br/> |[<span data-ttu-id="352ab-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="352ab-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="352ab-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="352ab-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="352ab-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="352ab-109">**Schema file**</span></span> <br/> |<span data-ttu-id="352ab-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="352ab-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="352ab-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="352ab-111">**Document parts**</span></span> <br/> |<span data-ttu-id="352ab-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="352ab-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="352ab-113">Definição</span><span class="sxs-lookup"><span data-stu-id="352ab-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="352ab-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="352ab-114">Elements and attributes</span></span>

<span data-ttu-id="352ab-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="352ab-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="352ab-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="352ab-116">Parent elements</span></span>

|<span data-ttu-id="352ab-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="352ab-117">**Element**</span></span>|<span data-ttu-id="352ab-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="352ab-118">**Type**</span></span>|<span data-ttu-id="352ab-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="352ab-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="352ab-120">Validação</span><span class="sxs-lookup"><span data-stu-id="352ab-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="352ab-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="352ab-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="352ab-122">Armazena informações sobre a validação de diagrama do documento.</span><span class="sxs-lookup"><span data-stu-id="352ab-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="352ab-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="352ab-123">Child elements</span></span>

|<span data-ttu-id="352ab-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="352ab-124">**Element**</span></span>|<span data-ttu-id="352ab-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="352ab-125">**Type**</span></span>|<span data-ttu-id="352ab-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="352ab-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="352ab-127">Problema</span><span class="sxs-lookup"><span data-stu-id="352ab-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="352ab-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="352ab-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="352ab-129">Representa uma questão de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="352ab-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="352ab-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="352ab-130">Attributes</span></span>

<span data-ttu-id="352ab-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="352ab-131">None.</span></span>
  

