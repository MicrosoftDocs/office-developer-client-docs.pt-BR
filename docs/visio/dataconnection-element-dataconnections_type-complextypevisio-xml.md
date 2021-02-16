---
title: Elemento DataConnection (DataConnections_Type complexType) (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Resume a comunicação entre um ou mais objetos DataRecordset e uma fonte de dados não XML.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538400"
---
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a><span data-ttu-id="20ae4-103">Elemento DataConnection (DataConnections_Type complexType) (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="20ae4-103">DataConnection element (DataConnections_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="20ae4-104">Resume a comunicação entre um ou mais objetos **DataRecordset** e uma fonte de dados não XML.</span><span class="sxs-lookup"><span data-stu-id="20ae4-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="20ae4-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="20ae4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20ae4-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="20ae4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="20ae4-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="20ae4-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="20ae4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="20ae4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="20ae4-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="20ae4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="20ae4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="20ae4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="20ae4-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="20ae4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="20ae4-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="20ae4-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="20ae4-113">Definição</span><span class="sxs-lookup"><span data-stu-id="20ae4-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="20ae4-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="20ae4-114">Elements and attributes</span></span>

<span data-ttu-id="20ae4-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="20ae4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="20ae4-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="20ae4-116">Parent elements</span></span>

|<span data-ttu-id="20ae4-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="20ae4-117">**Element**</span></span>|<span data-ttu-id="20ae4-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="20ae4-118">**Type**</span></span>|<span data-ttu-id="20ae4-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="20ae4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="20ae4-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="20ae4-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="20ae4-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="20ae4-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="20ae4-122">Contém os elementos **DataConnection** para o documento.</span><span class="sxs-lookup"><span data-stu-id="20ae4-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="20ae4-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="20ae4-123">Child elements</span></span>

<span data-ttu-id="20ae4-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="20ae4-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20ae4-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="20ae4-125">Attributes</span></span>

|<span data-ttu-id="20ae4-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="20ae4-126">**Attribute**</span></span>|<span data-ttu-id="20ae4-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="20ae4-127">**Type**</span></span>|<span data-ttu-id="20ae4-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="20ae4-128">**Required**</span></span>|<span data-ttu-id="20ae4-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="20ae4-129">**Description**</span></span>|<span data-ttu-id="20ae4-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="20ae4-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="20ae4-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="20ae4-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="20ae4-132">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="20ae4-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="20ae4-133">opcional</span><span class="sxs-lookup"><span data-stu-id="20ae4-133">optional</span></span>  <br/> |<span data-ttu-id="20ae4-134">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="20ae4-134">The default value is false.</span></span> <span data-ttu-id="20ae4-135">Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="20ae4-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="20ae4-136">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="20ae4-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="20ae4-137">Comando</span><span class="sxs-lookup"><span data-stu-id="20ae4-137">Command</span></span>  <br/> |<span data-ttu-id="20ae4-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="20ae4-138">xsd:string</span></span>  <br/> |<span data-ttu-id="20ae4-139">opcional</span><span class="sxs-lookup"><span data-stu-id="20ae4-139">optional</span></span>  <br/> |<span data-ttu-id="20ae4-140">A cadeia de caracteres de comando usada para consultar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="20ae4-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="20ae4-141">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="20ae4-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="20ae4-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="20ae4-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="20ae4-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="20ae4-143">xsd:string</span></span>  <br/> |<span data-ttu-id="20ae4-144">opcional</span><span class="sxs-lookup"><span data-stu-id="20ae4-144">optional</span></span>  <br/> |<span data-ttu-id="20ae4-145">A cadeia de conexão que define os parâmetros necessários para se conectar a uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="20ae4-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="20ae4-146">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="20ae4-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="20ae4-147">FileName</span><span class="sxs-lookup"><span data-stu-id="20ae4-147">FileName</span></span>  <br/> |<span data-ttu-id="20ae4-148">xsd:string</span><span class="sxs-lookup"><span data-stu-id="20ae4-148">xsd:string</span></span>  <br/> |<span data-ttu-id="20ae4-149">obrigatório</span><span class="sxs-lookup"><span data-stu-id="20ae4-149">required</span></span>  <br/> |<span data-ttu-id="20ae4-150">O nome do arquivo de conexão.</span><span class="sxs-lookup"><span data-stu-id="20ae4-150">The name of the connection file.</span></span> <span data-ttu-id="20ae4-151">Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="20ae4-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="20ae4-152">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="20ae4-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="20ae4-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="20ae4-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="20ae4-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="20ae4-154">xsd:string</span></span>  <br/> |<span data-ttu-id="20ae4-155">opcional</span><span class="sxs-lookup"><span data-stu-id="20ae4-155">optional</span></span>  <br/> |<span data-ttu-id="20ae4-156">Um nome fornecido pelo usuário para a conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="20ae4-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="20ae4-157">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="20ae4-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="20ae4-158">ID</span><span class="sxs-lookup"><span data-stu-id="20ae4-158">ID</span></span>  <br/> |<span data-ttu-id="20ae4-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="20ae4-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="20ae4-160">obrigatório</span><span class="sxs-lookup"><span data-stu-id="20ae4-160">required</span></span>  <br/> |<span data-ttu-id="20ae4-161">O ID atribuído pelo Visio para uma determinada conexão, exclusivo no documento.</span><span class="sxs-lookup"><span data-stu-id="20ae4-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="20ae4-162">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="20ae4-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="20ae4-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="20ae4-163">Timeout</span></span>  <br/> |<span data-ttu-id="20ae4-164">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="20ae4-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="20ae4-165">opcional</span><span class="sxs-lookup"><span data-stu-id="20ae4-165">optional</span></span>  <br/> |<span data-ttu-id="20ae4-166">O tempo de espera em minutos ao tentar estabelecer uma conexão antes de encerrar a tentativa.</span><span class="sxs-lookup"><span data-stu-id="20ae4-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="20ae4-167">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="20ae4-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

