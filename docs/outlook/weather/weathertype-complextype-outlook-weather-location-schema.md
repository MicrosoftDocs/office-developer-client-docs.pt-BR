---
title: weatherType complexType (Esquema de localização do clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Define os parâmetros sobre as condições meteorológicas para um local.
ms.openlocfilehash: c3d640789cb68891878c3dca5210ab9dea280180
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387710"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a><span data-ttu-id="2101f-103">weatherType complexType (Esquema de localização do clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="2101f-103">weatherType complexType (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="2101f-104">Define os parâmetros sobre as condições meteorológicas para um local.</span><span class="sxs-lookup"><span data-stu-id="2101f-104">Defines the parameters about the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="2101f-105">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="2101f-105">Type: Information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2101f-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2101f-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="2101f-107">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2101f-107">**Schema file**</span></span> <br/> |<span data-ttu-id="2101f-108">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="2101f-108">getweatherlocation.xsd</span></span>  <br/> |
|<span data-ttu-id="2101f-109">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="2101f-109">**Extension base**</span></span> <br/> |<span data-ttu-id="2101f-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2101f-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2101f-111">Definição</span><span class="sxs-lookup"><span data-stu-id="2101f-111">Definition</span></span>

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="2101f-112">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2101f-112">Elements and attributes</span></span>

<span data-ttu-id="2101f-113">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2101f-113">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2101f-114">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2101f-114">Child elements</span></span>

<span data-ttu-id="2101f-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2101f-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2101f-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="2101f-116">Attributes</span></span>

|<span data-ttu-id="2101f-117">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="2101f-117">**Attribute**</span></span>|<span data-ttu-id="2101f-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2101f-118">**Type**</span></span>|<span data-ttu-id="2101f-119">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="2101f-119">**Required**</span></span>|<span data-ttu-id="2101f-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2101f-120">**Description**</span></span>|<span data-ttu-id="2101f-121">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="2101f-121">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2101f-122">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="2101f-122">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="2101f-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="2101f-123">xs:string</span></span>  <br/> |<span data-ttu-id="2101f-124">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2101f-124">required</span></span>  <br/> |<span data-ttu-id="2101f-125">Especifica um código associado ao local para distinguir vários locais com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="2101f-125">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="2101f-126">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="2101f-126">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="2101f-127">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="2101f-127">weatherlocationname</span></span>  <br/> |<span data-ttu-id="2101f-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="2101f-128">xs:string</span></span>  <br/> |<span data-ttu-id="2101f-129">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2101f-129">required</span></span>  <br/> |<span data-ttu-id="2101f-130">Especifica o nome do local.</span><span class="sxs-lookup"><span data-stu-id="2101f-130">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="2101f-131">Um valor do tipo xs:string</span><span class="sxs-lookup"><span data-stu-id="2101f-131">A value of the type xs:string</span></span>  <br/> |
   

