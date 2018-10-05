---
title: Elemento de problemas (Validation_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Contém todos os elementos de problema para o documento.
ms.openlocfilehash: da3156e34af1536fab39d3d4949acac1efe67264
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400576"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="5130c-103">Elemento de problemas (Validation_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="5130c-103">Issues element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="5130c-104">Contém todos os elementos de problema para o documento.</span><span class="sxs-lookup"><span data-stu-id="5130c-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5130c-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="5130c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5130c-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="5130c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5130c-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="5130c-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5130c-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="5130c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5130c-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="5130c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5130c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5130c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5130c-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="5130c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5130c-112">Validation.XML</span><span class="sxs-lookup"><span data-stu-id="5130c-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5130c-113">Definição</span><span class="sxs-lookup"><span data-stu-id="5130c-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5130c-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="5130c-114">Elements and attributes</span></span>

<span data-ttu-id="5130c-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="5130c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5130c-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5130c-116">Parent elements</span></span>

|<span data-ttu-id="5130c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5130c-117">**Element**</span></span>|<span data-ttu-id="5130c-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5130c-118">**Type**</span></span>|<span data-ttu-id="5130c-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5130c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5130c-120">Validação</span><span class="sxs-lookup"><span data-stu-id="5130c-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="5130c-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="5130c-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5130c-122">Armazena informações sobre a validação de diagrama do documento.</span><span class="sxs-lookup"><span data-stu-id="5130c-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5130c-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5130c-123">Child elements</span></span>

|<span data-ttu-id="5130c-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5130c-124">**Element**</span></span>|<span data-ttu-id="5130c-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5130c-125">**Type**</span></span>|<span data-ttu-id="5130c-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5130c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5130c-127">Problema</span><span class="sxs-lookup"><span data-stu-id="5130c-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5130c-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="5130c-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5130c-129">Representa uma questão de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="5130c-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5130c-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="5130c-130">Attributes</span></span>

<span data-ttu-id="5130c-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5130c-131">None.</span></span>
  

