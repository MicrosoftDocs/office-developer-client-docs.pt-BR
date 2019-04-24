---
title: Elemento StyleSheets (VisioDocument_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da26de4b-3e5b-326b-de46-e8c542b74f02
description: Contém uma coleção de elementos StyleSheet para o documento.
ms.openlocfilehash: 4aae3bcbecec34d961f2d14fd6d3865e7cd332f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329782"
---
# <a name="stylesheets-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="17cc6-103">Elemento StyleSheets (VisioDocument_Type complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="17cc6-103">StyleSheets element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="17cc6-104">Contém uma coleção de elementos StyleSheet para o documento.</span><span class="sxs-lookup"><span data-stu-id="17cc6-104">Contains a collection of StyleSheet elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17cc6-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="17cc6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17cc6-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="17cc6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="17cc6-107">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="17cc6-107">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="17cc6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="17cc6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="17cc6-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="17cc6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="17cc6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="17cc6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="17cc6-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="17cc6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="17cc6-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="17cc6-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="17cc6-113">Definição</span><span class="sxs-lookup"><span data-stu-id="17cc6-113">Definition</span></span>

```XML
< xs:element name="StyleSheets" type="StyleSheets_Type" minOccurs="0" maxOccurs="1" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="17cc6-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="17cc6-114">Elements and attributes</span></span>

<span data-ttu-id="17cc6-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="17cc6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="17cc6-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="17cc6-116">Parent elements</span></span>

|<span data-ttu-id="17cc6-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="17cc6-117">**Element**</span></span>|<span data-ttu-id="17cc6-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="17cc6-118">**Type**</span></span>|<span data-ttu-id="17cc6-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="17cc6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17cc6-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="17cc6-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="17cc6-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="17cc6-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="17cc6-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="17cc6-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="17cc6-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="17cc6-123">Child elements</span></span>

|<span data-ttu-id="17cc6-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="17cc6-124">**Element**</span></span>|<span data-ttu-id="17cc6-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="17cc6-125">**Type**</span></span>|<span data-ttu-id="17cc6-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="17cc6-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17cc6-127">StyleSheet</span><span class="sxs-lookup"><span data-stu-id="17cc6-127">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17cc6-128">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="17cc6-128">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="17cc6-129">Representa um estilo definido em um documento.</span><span class="sxs-lookup"><span data-stu-id="17cc6-129">Represents a style defined in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="17cc6-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="17cc6-130">Attributes</span></span>

<span data-ttu-id="17cc6-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="17cc6-131">None.</span></span>
  

