---
title: Elemento Colors (VisioDocument_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Contém a tabela de cor do documento.
ms.openlocfilehash: bd46f58dfbb8a596717662b9a0524d59bb508270
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358755"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="6dfce-103">Elemento Colors (VisioDocument_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="6dfce-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6dfce-104">Contém a tabela de cor do documento.</span><span class="sxs-lookup"><span data-stu-id="6dfce-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6dfce-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="6dfce-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6dfce-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="6dfce-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6dfce-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="6dfce-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6dfce-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6dfce-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6dfce-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="6dfce-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6dfce-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6dfce-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6dfce-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="6dfce-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6dfce-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="6dfce-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6dfce-113">Definição</span><span class="sxs-lookup"><span data-stu-id="6dfce-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6dfce-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="6dfce-114">Elements and attributes</span></span>

<span data-ttu-id="6dfce-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="6dfce-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6dfce-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6dfce-116">Parent elements</span></span>

|<span data-ttu-id="6dfce-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6dfce-117">**Element**</span></span>|<span data-ttu-id="6dfce-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6dfce-118">**Type**</span></span>|<span data-ttu-id="6dfce-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6dfce-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6dfce-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="6dfce-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="6dfce-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="6dfce-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6dfce-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="6dfce-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6dfce-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6dfce-123">Child elements</span></span>

|<span data-ttu-id="6dfce-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6dfce-124">**Element**</span></span>|<span data-ttu-id="6dfce-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6dfce-125">**Type**</span></span>|<span data-ttu-id="6dfce-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6dfce-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6dfce-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="6dfce-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6dfce-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="6dfce-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6dfce-129">Contém uma entrada de tabela de cor.</span><span class="sxs-lookup"><span data-stu-id="6dfce-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6dfce-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="6dfce-130">Attributes</span></span>

<span data-ttu-id="6dfce-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6dfce-131">None.</span></span>
  

