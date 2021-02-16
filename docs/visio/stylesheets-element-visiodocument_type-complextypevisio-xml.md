---
title: Elemento StyleSheets (VisioDocument_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da26de4b-3e5b-326b-de46-e8c542b74f02
description: Contém uma coleção de elementos StyleSheet para o documento.
ms.openlocfilehash: 363cb102fb545ffd20601bf0125c22aeb06defa8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541985"
---
# <a name="stylesheets-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="f134e-103">Elemento StyleSheets (VisioDocument_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="f134e-103">StyleSheets element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f134e-104">Contém uma coleção de elementos StyleSheet para o documento.</span><span class="sxs-lookup"><span data-stu-id="f134e-104">Contains a collection of StyleSheet elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f134e-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="f134e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f134e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f134e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f134e-107">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="f134e-107">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f134e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f134e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f134e-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f134e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f134e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f134e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f134e-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="f134e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f134e-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="f134e-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f134e-113">Definição</span><span class="sxs-lookup"><span data-stu-id="f134e-113">Definition</span></span>

```XML
< xs:element name="StyleSheets" type="StyleSheets_Type" minOccurs="0" maxOccurs="1" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f134e-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f134e-114">Elements and attributes</span></span>

<span data-ttu-id="f134e-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f134e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f134e-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f134e-116">Parent elements</span></span>

|<span data-ttu-id="f134e-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f134e-117">**Element**</span></span>|<span data-ttu-id="f134e-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f134e-118">**Type**</span></span>|<span data-ttu-id="f134e-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f134e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f134e-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="f134e-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="f134e-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="f134e-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f134e-122">O elemento raiz de um documento do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="f134e-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f134e-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f134e-123">Child elements</span></span>

|<span data-ttu-id="f134e-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f134e-124">**Element**</span></span>|<span data-ttu-id="f134e-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f134e-125">**Type**</span></span>|<span data-ttu-id="f134e-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f134e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f134e-127">StyleSheet</span><span class="sxs-lookup"><span data-stu-id="f134e-127">StyleSheet</span></span>](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f134e-128">StyleSheet_Type</span><span class="sxs-lookup"><span data-stu-id="f134e-128">StyleSheet_Type</span></span>](stylesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f134e-129">Representa um estilo definido em um documento.</span><span class="sxs-lookup"><span data-stu-id="f134e-129">Represents a style defined in a document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f134e-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="f134e-130">Attributes</span></span>

<span data-ttu-id="f134e-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f134e-131">None.</span></span>
  

