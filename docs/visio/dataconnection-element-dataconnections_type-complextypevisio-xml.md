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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344622"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="64e05-103">Elemento DataConnection (DataConnections_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="64e05-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="64e05-104">Resume a comunicação entre um ou mais objetos **DataRecordset** e uma fonte de dados não XML.</span><span class="sxs-lookup"><span data-stu-id="64e05-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="64e05-105">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="64e05-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64e05-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="64e05-106">**Element type**</span></span> <br/> |[<span data-ttu-id="64e05-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="64e05-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="64e05-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="64e05-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="64e05-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="64e05-109">**Schema file**</span></span> <br/> |<span data-ttu-id="64e05-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="64e05-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="64e05-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="64e05-111">**Document parts**</span></span> <br/> |<span data-ttu-id="64e05-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="64e05-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="64e05-113">Definição</span><span class="sxs-lookup"><span data-stu-id="64e05-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="64e05-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="64e05-114">Elements and attributes</span></span>

<span data-ttu-id="64e05-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="64e05-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="64e05-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="64e05-116">Parent elements</span></span>

|<span data-ttu-id="64e05-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="64e05-117">**Element**</span></span>|<span data-ttu-id="64e05-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="64e05-118">**Type**</span></span>|<span data-ttu-id="64e05-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="64e05-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="64e05-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="64e05-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="64e05-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="64e05-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="64e05-122">Contém os elementos **DataConnection** para o documento.</span><span class="sxs-lookup"><span data-stu-id="64e05-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="64e05-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="64e05-123">Child elements</span></span>

<span data-ttu-id="64e05-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="64e05-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64e05-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="64e05-125">Attributes</span></span>

|<span data-ttu-id="64e05-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="64e05-126">**Attribute**</span></span>|<span data-ttu-id="64e05-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="64e05-127">**Type**</span></span>|<span data-ttu-id="64e05-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="64e05-128">**Required**</span></span>|<span data-ttu-id="64e05-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="64e05-129">**Description**</span></span>|<span data-ttu-id="64e05-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="64e05-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="64e05-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="64e05-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="64e05-132">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="64e05-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="64e05-133">opcional</span><span class="sxs-lookup"><span data-stu-id="64e05-133">optional</span></span>  <br/> |<span data-ttu-id="64e05-134">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="64e05-134">The default value is false.</span></span> <span data-ttu-id="64e05-135">Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="64e05-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="64e05-136">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="64e05-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="64e05-137">Comando</span><span class="sxs-lookup"><span data-stu-id="64e05-137">Command</span></span>  <br/> |<span data-ttu-id="64e05-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="64e05-138">xsd:string</span></span>  <br/> |<span data-ttu-id="64e05-139">opcional</span><span class="sxs-lookup"><span data-stu-id="64e05-139">optional</span></span>  <br/> |<span data-ttu-id="64e05-140">A cadeia de caracteres de comando usada para consultar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="64e05-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="64e05-141">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="64e05-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="64e05-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="64e05-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="64e05-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="64e05-143">xsd:string</span></span>  <br/> |<span data-ttu-id="64e05-144">opcional</span><span class="sxs-lookup"><span data-stu-id="64e05-144">optional</span></span>  <br/> |<span data-ttu-id="64e05-145">A cadeia de conexão que define os parâmetros necessários para se conectar a uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="64e05-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="64e05-146">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="64e05-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="64e05-147">FileName</span><span class="sxs-lookup"><span data-stu-id="64e05-147">FileName</span></span>  <br/> |<span data-ttu-id="64e05-148">xsd:string</span><span class="sxs-lookup"><span data-stu-id="64e05-148">xsd:string</span></span>  <br/> |<span data-ttu-id="64e05-149">obrigatório</span><span class="sxs-lookup"><span data-stu-id="64e05-149">required</span></span>  <br/> |<span data-ttu-id="64e05-150">O nome do arquivo de conexão.</span><span class="sxs-lookup"><span data-stu-id="64e05-150">The name of the connection file.</span></span> <span data-ttu-id="64e05-151">Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="64e05-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="64e05-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="64e05-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="64e05-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="64e05-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="64e05-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="64e05-154">xsd:string</span></span>  <br/> |<span data-ttu-id="64e05-155">opcional</span><span class="sxs-lookup"><span data-stu-id="64e05-155">optional</span></span>  <br/> |<span data-ttu-id="64e05-156">Um nome fornecido pelo usuário para a conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="64e05-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="64e05-157">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="64e05-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="64e05-158">ID</span><span class="sxs-lookup"><span data-stu-id="64e05-158">ID</span></span>  <br/> |<span data-ttu-id="64e05-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64e05-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64e05-160">obrigatório</span><span class="sxs-lookup"><span data-stu-id="64e05-160">required</span></span>  <br/> |<span data-ttu-id="64e05-161">O ID atribuído pelo Visio para uma determinada conexão, exclusivo no documento.</span><span class="sxs-lookup"><span data-stu-id="64e05-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="64e05-162">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="64e05-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="64e05-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="64e05-163">Timeout</span></span>  <br/> |<span data-ttu-id="64e05-164">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="64e05-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="64e05-165">opcional</span><span class="sxs-lookup"><span data-stu-id="64e05-165">optional</span></span>  <br/> |<span data-ttu-id="64e05-166">O tempo de espera em minutos ao tentar estabelecer uma conexão antes de encerrar a tentativa.</span><span class="sxs-lookup"><span data-stu-id="64e05-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="64e05-167">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="64e05-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

