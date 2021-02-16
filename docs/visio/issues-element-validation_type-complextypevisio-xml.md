---
title: Elemento Issues (Validation_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Contém todos os elementos Issue do documento.
ms.openlocfilehash: dced8ab94b51535a47415794954b5b3062963ede
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542937"
---
# <a name="issues-element-validation_type-complextype-visio-xml"></a><span data-ttu-id="17cc5-103">Elemento Issues (Validation_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="17cc5-103">Issues element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="17cc5-104">Contém todos os elementos Issue do documento.</span><span class="sxs-lookup"><span data-stu-id="17cc5-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17cc5-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="17cc5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17cc5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="17cc5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="17cc5-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="17cc5-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="17cc5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="17cc5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="17cc5-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="17cc5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="17cc5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="17cc5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="17cc5-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="17cc5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="17cc5-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="17cc5-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="17cc5-113">Definição</span><span class="sxs-lookup"><span data-stu-id="17cc5-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="17cc5-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="17cc5-114">Elements and attributes</span></span>

<span data-ttu-id="17cc5-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="17cc5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="17cc5-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="17cc5-116">Parent elements</span></span>

|<span data-ttu-id="17cc5-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="17cc5-117">**Element**</span></span>|<span data-ttu-id="17cc5-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="17cc5-118">**Type**</span></span>|<span data-ttu-id="17cc5-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="17cc5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17cc5-120">Validation</span><span class="sxs-lookup"><span data-stu-id="17cc5-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="17cc5-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="17cc5-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="17cc5-122">Armazena informações sobre a validação de diagrama do documento.</span><span class="sxs-lookup"><span data-stu-id="17cc5-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="17cc5-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="17cc5-123">Child elements</span></span>

|<span data-ttu-id="17cc5-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="17cc5-124">**Element**</span></span>|<span data-ttu-id="17cc5-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="17cc5-125">**Type**</span></span>|<span data-ttu-id="17cc5-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="17cc5-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17cc5-127">Problema</span><span class="sxs-lookup"><span data-stu-id="17cc5-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17cc5-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="17cc5-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="17cc5-129">Representa uma única questão de validação no documento.</span><span class="sxs-lookup"><span data-stu-id="17cc5-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="17cc5-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="17cc5-130">Attributes</span></span>

<span data-ttu-id="17cc5-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="17cc5-131">None.</span></span>
  

