---
title: Elemento Masters (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Contém os elementos mestres do documento.
ms.openlocfilehash: ea2cee2f9845f8a72220081617a11cf4f72dafd1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341423"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="0ea1f-103">Elemento Masters (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="0ea1f-103">Masters element ('Visio XML')</span></span>

<span data-ttu-id="0ea1f-104">Contém os elementos mestres do documento.</span><span class="sxs-lookup"><span data-stu-id="0ea1f-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ea1f-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="0ea1f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ea1f-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="0ea1f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0ea1f-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="0ea1f-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0ea1f-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0ea1f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0ea1f-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0ea1f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0ea1f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="0ea1f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0ea1f-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="0ea1f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0ea1f-112">Masters. xml</span><span class="sxs-lookup"><span data-stu-id="0ea1f-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0ea1f-113">Definição</span><span class="sxs-lookup"><span data-stu-id="0ea1f-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0ea1f-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="0ea1f-114">Elements and attributes</span></span>

<span data-ttu-id="0ea1f-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="0ea1f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0ea1f-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="0ea1f-116">Parent elements</span></span>

<span data-ttu-id="0ea1f-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0ea1f-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0ea1f-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0ea1f-118">Child elements</span></span>

|<span data-ttu-id="0ea1f-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0ea1f-119">**Element**</span></span>|<span data-ttu-id="0ea1f-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0ea1f-120">**Type**</span></span>|<span data-ttu-id="0ea1f-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0ea1f-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0ea1f-122">Master</span><span class="sxs-lookup"><span data-stu-id="0ea1f-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0ea1f-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="0ea1f-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0ea1f-124">Contém elementos que definem um mestre para o documento.</span><span class="sxs-lookup"><span data-stu-id="0ea1f-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="0ea1f-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="0ea1f-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0ea1f-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="0ea1f-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0ea1f-127">Especifica um atalho mestre definido no documento.</span><span class="sxs-lookup"><span data-stu-id="0ea1f-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0ea1f-128">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ea1f-128">Attributes</span></span>

<span data-ttu-id="0ea1f-129">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="0ea1f-129">None.</span></span>
  

