---
title: Elemento Colors (VisioDocument_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Contém a tabela de cor do documento.
ms.openlocfilehash: 6f18926961583e09f83dd7921ca140c07a60ecc3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540172"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="1300a-103">Elemento Colors (VisioDocument_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="1300a-103">Colors element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="1300a-104">Contém a tabela de cor do documento.</span><span class="sxs-lookup"><span data-stu-id="1300a-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1300a-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="1300a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1300a-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="1300a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1300a-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="1300a-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1300a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1300a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1300a-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="1300a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1300a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1300a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1300a-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="1300a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1300a-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="1300a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1300a-113">Definição</span><span class="sxs-lookup"><span data-stu-id="1300a-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1300a-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="1300a-114">Elements and attributes</span></span>

<span data-ttu-id="1300a-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="1300a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1300a-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="1300a-116">Parent elements</span></span>

|<span data-ttu-id="1300a-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1300a-117">**Element**</span></span>|<span data-ttu-id="1300a-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1300a-118">**Type**</span></span>|<span data-ttu-id="1300a-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1300a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1300a-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="1300a-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="1300a-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="1300a-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1300a-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="1300a-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1300a-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1300a-123">Child elements</span></span>

|<span data-ttu-id="1300a-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1300a-124">**Element**</span></span>|<span data-ttu-id="1300a-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1300a-125">**Type**</span></span>|<span data-ttu-id="1300a-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1300a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1300a-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="1300a-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1300a-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="1300a-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1300a-129">Contém uma entrada de tabela de cor.</span><span class="sxs-lookup"><span data-stu-id="1300a-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1300a-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="1300a-130">Attributes</span></span>

<span data-ttu-id="1300a-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1300a-131">None.</span></span>
  

