---
title: elemento WeatherData (esquema de local de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Define o elemento de clima.
ms.openlocfilehash: 5a3d0ed0fbf8d06472a6d9af727a41d97c0231cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771067"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="2cd1d-103">elemento WeatherData (esquema de local de clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="2cd1d-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="2cd1d-104">Define o elemento de clima.</span><span class="sxs-lookup"><span data-stu-id="2cd1d-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2cd1d-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="2cd1d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2cd1d-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="2cd1d-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="2cd1d-108">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-108">**Schema file**</span></span> <br/> |<span data-ttu-id="2cd1d-109">getweatherlocation.xsd</span><span class="sxs-lookup"><span data-stu-id="2cd1d-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2cd1d-110">Definição</span><span class="sxs-lookup"><span data-stu-id="2cd1d-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType" maxOccurs="unbounded"
      >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2cd1d-111">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2cd1d-111">Elements and attributes</span></span>

<span data-ttu-id="2cd1d-112">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2cd1d-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2cd1d-113">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2cd1d-113">Parent elements</span></span>

<span data-ttu-id="2cd1d-114">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2cd1d-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2cd1d-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2cd1d-115">Child elements</span></span>

|<span data-ttu-id="2cd1d-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-116">**Element**</span></span>|<span data-ttu-id="2cd1d-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-117">**Type**</span></span>|<span data-ttu-id="2cd1d-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2cd1d-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2cd1d-119">clima</span><span class="sxs-lookup"><span data-stu-id="2cd1d-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="2cd1d-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="2cd1d-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="2cd1d-121">Especifica o local de clima de relatório no.</span><span class="sxs-lookup"><span data-stu-id="2cd1d-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2cd1d-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="2cd1d-122">Attributes</span></span>

<span data-ttu-id="2cd1d-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2cd1d-123">None.</span></span>
  

