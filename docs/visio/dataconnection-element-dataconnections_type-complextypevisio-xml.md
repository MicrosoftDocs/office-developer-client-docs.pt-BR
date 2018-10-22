---
title: Elemento DataConnection (DataConnections_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Resume a comunicação entre um ou mais objetos DataRecordset e uma fonte de dados não XML.
ms.openlocfilehash: 0073c329ec9149263530421531522c4d0b95633d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399421"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="13a20-103">Elemento DataConnection (DataConnections_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="13a20-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="13a20-104">Resume a comunicação entre um ou mais objetos **DataRecordset** e uma fonte de dados não XML.</span><span class="sxs-lookup"><span data-stu-id="13a20-104">Abstracts communication between one or more DataRecordset objects and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="13a20-105">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="13a20-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13a20-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="13a20-106">**Element type**</span></span> <br/> |[<span data-ttu-id="13a20-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="13a20-107">DataConnection_Type complexType</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="13a20-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="13a20-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="13a20-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="13a20-109">**Schema file**</span></span> <br/> |<span data-ttu-id="13a20-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="13a20-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="13a20-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="13a20-111">**Document parts**</span></span> <br/> |<span data-ttu-id="13a20-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="13a20-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="13a20-113">Definição</span><span class="sxs-lookup"><span data-stu-id="13a20-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="13a20-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="13a20-114">Elements and attributes</span></span>

<span data-ttu-id="13a20-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="13a20-115">
    If the schema defines specific requirements, such as \*\*sequence\*\*, \*\*minOccurs**,
    \*\*maxOccurs\**, and
    \*\*choice\*\*, see the definition section.
</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="13a20-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="13a20-116">Parent elements</span></span>

|<span data-ttu-id="13a20-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="13a20-117">**Element**</span></span>|<span data-ttu-id="13a20-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="13a20-118">**Type**</span></span>|<span data-ttu-id="13a20-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="13a20-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="13a20-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="13a20-120">DataConnections element</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="13a20-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="13a20-121">DataConnections_Type complexType</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="13a20-122">Contém os elementos **DataConnection** para o documento.</span><span class="sxs-lookup"><span data-stu-id="13a20-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="13a20-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="13a20-123">Child elements</span></span>

<span data-ttu-id="13a20-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="13a20-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13a20-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="13a20-125">Attributes</span></span>

|<span data-ttu-id="13a20-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="13a20-126">**Attribute**</span></span>|<span data-ttu-id="13a20-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="13a20-127">**Type**</span></span>|<span data-ttu-id="13a20-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="13a20-128">**Required**</span></span>|<span data-ttu-id="13a20-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="13a20-129">**Description**</span></span>|<span data-ttu-id="13a20-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="13a20-130">**Possible values:**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="13a20-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="13a20-131">AlwaysUseConnectionFile Property</span></span>  <br/> |<span data-ttu-id="13a20-132">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="13a20-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="13a20-133">opcional</span><span class="sxs-lookup"><span data-stu-id="13a20-133">optional</span></span>  <br/> |<span data-ttu-id="13a20-134">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="13a20-134">The default value is False.</span></span> <span data-ttu-id="13a20-135">Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="13a20-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="13a20-136">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="13a20-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="13a20-137">Comando</span><span class="sxs-lookup"><span data-stu-id="13a20-137">Command</span></span>  <br/> |<span data-ttu-id="13a20-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="13a20-138">xsd:string</span></span>  <br/> |<span data-ttu-id="13a20-139">opcional</span><span class="sxs-lookup"><span data-stu-id="13a20-139">optional</span></span>  <br/> |<span data-ttu-id="13a20-140">A cadeia de caracteres de comando usada para consultar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="13a20-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="13a20-141">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="13a20-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13a20-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="13a20-142">ConnectionString Property</span></span>  <br/> |<span data-ttu-id="13a20-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="13a20-143">xsd:string</span></span>  <br/> |<span data-ttu-id="13a20-144">opcional</span><span class="sxs-lookup"><span data-stu-id="13a20-144">optional</span></span>  <br/> |<span data-ttu-id="13a20-145">A cadeia de conexão que define os parâmetros necessários para se conectar a uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="13a20-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="13a20-146">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="13a20-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13a20-147">FileName</span><span class="sxs-lookup"><span data-stu-id="13a20-147">fileName</span></span>  <br/> |<span data-ttu-id="13a20-148">xsd:string</span><span class="sxs-lookup"><span data-stu-id="13a20-148">xsd:string</span></span>  <br/> |<span data-ttu-id="13a20-149">obrigatório</span><span class="sxs-lookup"><span data-stu-id="13a20-149">required</span></span>  <br/> |<span data-ttu-id="13a20-150">O nome do arquivo de conexão.</span><span class="sxs-lookup"><span data-stu-id="13a20-150">The name of the ODC connection file to use.</span></span> <span data-ttu-id="13a20-151">Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="13a20-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="13a20-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="13a20-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13a20-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="13a20-153">FriendlyName element</span></span>  <br/> |<span data-ttu-id="13a20-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="13a20-154">xsd:string</span></span>  <br/> |<span data-ttu-id="13a20-155">opcional</span><span class="sxs-lookup"><span data-stu-id="13a20-155">optional</span></span>  <br/> |<span data-ttu-id="13a20-156">Um nome fornecido pelo usuário para a conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="13a20-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="13a20-157">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="13a20-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="13a20-158">ID</span><span class="sxs-lookup"><span data-stu-id="13a20-158">ID</span></span>  <br/> |<span data-ttu-id="13a20-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="13a20-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="13a20-160">obrigatório</span><span class="sxs-lookup"><span data-stu-id="13a20-160">required</span></span>  <br/> |<span data-ttu-id="13a20-161">O ID atribuído pelo Visio para uma determinada conexão, exclusivo no documento.</span><span class="sxs-lookup"><span data-stu-id="13a20-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="13a20-162">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="13a20-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="13a20-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="13a20-163">Timeout</span></span>  <br/> |<span data-ttu-id="13a20-164">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="13a20-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="13a20-165">opcional</span><span class="sxs-lookup"><span data-stu-id="13a20-165">optional</span></span>  <br/> |<span data-ttu-id="13a20-166">O tempo de espera em minutos ao tentar estabelecer uma conexão antes de encerrar a tentativa.</span><span class="sxs-lookup"><span data-stu-id="13a20-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="13a20-167">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="13a20-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

