---
title: Elemento de conexões de dados ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Contém os elementos de DataConnection para o documento.
ms.openlocfilehash: 4de4429985ab0417341224f7f9e267a9873c6504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771656"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="233a5-103">Elemento de conexões de dados ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="233a5-103">DataConnections element ('Visio XML')</span></span>

<span data-ttu-id="233a5-104">Contém os elementos de **DataConnection** para o documento.</span><span class="sxs-lookup"><span data-stu-id="233a5-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="233a5-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="233a5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="233a5-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="233a5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="233a5-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="233a5-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="233a5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="233a5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="233a5-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="233a5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="233a5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="233a5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="233a5-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="233a5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="233a5-112">Connections.XML</span><span class="sxs-lookup"><span data-stu-id="233a5-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="233a5-113">Definição</span><span class="sxs-lookup"><span data-stu-id="233a5-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="233a5-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="233a5-114">Elements and attributes</span></span>

<span data-ttu-id="233a5-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="233a5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="233a5-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="233a5-116">Parent elements</span></span>

<span data-ttu-id="233a5-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="233a5-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="233a5-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="233a5-118">Child elements</span></span>

|<span data-ttu-id="233a5-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="233a5-119">**Element**</span></span>|<span data-ttu-id="233a5-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="233a5-120">**Type**</span></span>|<span data-ttu-id="233a5-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="233a5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="233a5-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="233a5-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="233a5-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="233a5-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="233a5-124">Resume a comunicação entre um ou mais elementos de **DataRecordset** e uma fonte de dados não-XML.</span><span class="sxs-lookup"><span data-stu-id="233a5-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="233a5-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="233a5-125">Attributes</span></span>

|<span data-ttu-id="233a5-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="233a5-126">**Attribute**</span></span>|<span data-ttu-id="233a5-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="233a5-127">**Type**</span></span>|<span data-ttu-id="233a5-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="233a5-128">**Required**</span></span>|<span data-ttu-id="233a5-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="233a5-129">**Description**</span></span>|<span data-ttu-id="233a5-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="233a5-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="233a5-131">NextID</span><span class="sxs-lookup"><span data-stu-id="233a5-131">NextID</span></span>  <br/> |<span data-ttu-id="233a5-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="233a5-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="233a5-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="233a5-133">required</span></span>  <br/> |<span data-ttu-id="233a5-134">A identificação disponível próxima para novas conexões.</span><span class="sxs-lookup"><span data-stu-id="233a5-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="233a5-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="233a5-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

