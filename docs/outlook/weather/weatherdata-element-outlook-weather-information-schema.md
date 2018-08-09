---
title: elemento WeatherData (esquema de informações de clima do Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: Define o elemento de clima.
ms.openlocfilehash: 689c390f621d18f680de9635c3d82711300f8030
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771068"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="2647e-103">elemento WeatherData (esquema de informações de clima do Outlook)</span><span class="sxs-lookup"><span data-stu-id="2647e-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="2647e-104">Define o elemento de clima.</span><span class="sxs-lookup"><span data-stu-id="2647e-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2647e-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="2647e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2647e-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="2647e-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="2647e-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2647e-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="2647e-108">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2647e-108">**Schema file**</span></span> <br/> |<span data-ttu-id="2647e-109">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="2647e-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2647e-110">Definição</span><span class="sxs-lookup"><span data-stu-id="2647e-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType">
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2647e-111">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2647e-111">Elements and attributes</span></span>

<span data-ttu-id="2647e-112">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2647e-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2647e-113">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="2647e-113">Parent elements</span></span>

<span data-ttu-id="2647e-114">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2647e-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2647e-115">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2647e-115">Child elements</span></span>

|<span data-ttu-id="2647e-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2647e-116">**Element**</span></span>|<span data-ttu-id="2647e-117">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2647e-117">**Type**</span></span>|<span data-ttu-id="2647e-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2647e-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2647e-119">clima</span><span class="sxs-lookup"><span data-stu-id="2647e-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="2647e-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="2647e-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="2647e-121">Especifica as condições de clima de um local.</span><span class="sxs-lookup"><span data-stu-id="2647e-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2647e-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="2647e-122">Attributes</span></span>

<span data-ttu-id="2647e-123">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2647e-123">None.</span></span>
  

