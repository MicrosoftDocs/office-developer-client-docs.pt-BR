---
title: Elemento DataConnections (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Contém os elementos DataConnection para o documento.
ms.openlocfilehash: 5d45d1dcd76524c2144336235e8277cd51f8a138
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539179"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="95ce0-103">Elemento DataConnections (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="95ce0-103">DataConnections element (Visio XML)</span></span>

<span data-ttu-id="95ce0-104">Contém os elementos **DataConnection** para o documento.</span><span class="sxs-lookup"><span data-stu-id="95ce0-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="95ce0-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="95ce0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95ce0-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="95ce0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="95ce0-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="95ce0-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="95ce0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="95ce0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="95ce0-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="95ce0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="95ce0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="95ce0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="95ce0-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="95ce0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="95ce0-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="95ce0-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95ce0-113">Definição</span><span class="sxs-lookup"><span data-stu-id="95ce0-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="95ce0-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="95ce0-114">Elements and attributes</span></span>

<span data-ttu-id="95ce0-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="95ce0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="95ce0-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="95ce0-116">Parent elements</span></span>

<span data-ttu-id="95ce0-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="95ce0-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95ce0-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="95ce0-118">Child elements</span></span>

|<span data-ttu-id="95ce0-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="95ce0-119">**Element**</span></span>|<span data-ttu-id="95ce0-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="95ce0-120">**Type**</span></span>|<span data-ttu-id="95ce0-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="95ce0-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95ce0-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="95ce0-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95ce0-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="95ce0-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95ce0-124">Resume a comunicação entre um ou mais objetos **DataRecordset** e uma fonte de dados não-XML.</span><span class="sxs-lookup"><span data-stu-id="95ce0-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="95ce0-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="95ce0-125">Attributes</span></span>

|<span data-ttu-id="95ce0-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="95ce0-126">**Attribute**</span></span>|<span data-ttu-id="95ce0-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="95ce0-127">**Type**</span></span>|<span data-ttu-id="95ce0-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="95ce0-128">**Required**</span></span>|<span data-ttu-id="95ce0-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="95ce0-129">**Description**</span></span>|<span data-ttu-id="95ce0-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="95ce0-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="95ce0-131">NextID</span><span class="sxs-lookup"><span data-stu-id="95ce0-131">NextID</span></span>  <br/> |<span data-ttu-id="95ce0-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="95ce0-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="95ce0-133">obrigatório</span><span class="sxs-lookup"><span data-stu-id="95ce0-133">required</span></span>  <br/> |<span data-ttu-id="95ce0-134">A próxima ID disponível para novas conexões.</span><span class="sxs-lookup"><span data-stu-id="95ce0-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="95ce0-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="95ce0-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

