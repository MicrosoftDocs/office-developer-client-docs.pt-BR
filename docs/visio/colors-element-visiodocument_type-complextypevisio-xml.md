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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400527"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="fb183-103">Elemento Colors (VisioDocument_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="fb183-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="fb183-104">Contém a tabela de cor do documento.</span><span class="sxs-lookup"><span data-stu-id="fb183-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fb183-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="fb183-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb183-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="fb183-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fb183-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="fb183-107">Colors_Type complexType</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fb183-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fb183-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fb183-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="fb183-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fb183-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fb183-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fb183-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="fb183-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fb183-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="fb183-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fb183-113">Definição</span><span class="sxs-lookup"><span data-stu-id="fb183-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fb183-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="fb183-114">Elements and attributes</span></span>

<span data-ttu-id="fb183-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="fb183-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fb183-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="fb183-116">Parent elements</span></span>

|<span data-ttu-id="fb183-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fb183-117">**Element**</span></span>|<span data-ttu-id="fb183-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fb183-118">**Type**</span></span>|<span data-ttu-id="fb183-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fb183-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fb183-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="fb183-120">VisioDocument element</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="fb183-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="fb183-121">VisioDocument_Type complexType</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fb183-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="fb183-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fb183-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fb183-123">Child elements</span></span>

|<span data-ttu-id="fb183-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fb183-124">**Element**</span></span>|<span data-ttu-id="fb183-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="fb183-125">**Type**</span></span>|<span data-ttu-id="fb183-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fb183-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fb183-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="fb183-127">ColorEntry element</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fb183-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="fb183-128">ColorEntry_Type complexType</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fb183-129">Contém uma entrada de tabela de cor.</span><span class="sxs-lookup"><span data-stu-id="fb183-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fb183-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="fb183-130">Attributes</span></span>

<span data-ttu-id="fb183-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fb183-131">None.</span></span>
  

