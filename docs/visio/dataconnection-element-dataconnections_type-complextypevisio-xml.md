---
title: Elemento de DataConnection (DataConnections_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Resume a comunicação entre um ou mais elementos de DataRecordset e uma fonte de dados não-XML.
ms.openlocfilehash: 74e15795e023517263d9b79e9f19557653e4e939
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771666"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="4240a-103">Elemento de DataConnection (DataConnections_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4240a-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4240a-104">Resume a comunicação entre um ou mais elementos de **DataRecordset** e uma fonte de dados não-XML.</span><span class="sxs-lookup"><span data-stu-id="4240a-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4240a-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="4240a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4240a-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="4240a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4240a-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="4240a-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4240a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4240a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4240a-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4240a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4240a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4240a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4240a-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="4240a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4240a-112">Connections.XML</span><span class="sxs-lookup"><span data-stu-id="4240a-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4240a-113">Definição</span><span class="sxs-lookup"><span data-stu-id="4240a-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4240a-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4240a-114">Elements and attributes</span></span>

<span data-ttu-id="4240a-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4240a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4240a-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="4240a-116">Parent elements</span></span>

|<span data-ttu-id="4240a-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4240a-117">**Element**</span></span>|<span data-ttu-id="4240a-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4240a-118">**Type**</span></span>|<span data-ttu-id="4240a-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4240a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4240a-120">Conexões de dados</span><span class="sxs-lookup"><span data-stu-id="4240a-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="4240a-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="4240a-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4240a-122">Contém os elementos de **DataConnection** para o documento.</span><span class="sxs-lookup"><span data-stu-id="4240a-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4240a-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4240a-123">Child elements</span></span>

<span data-ttu-id="4240a-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4240a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4240a-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="4240a-125">Attributes</span></span>

|<span data-ttu-id="4240a-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4240a-126">**Attribute**</span></span>|<span data-ttu-id="4240a-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4240a-127">**Type**</span></span>|<span data-ttu-id="4240a-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="4240a-128">**Required**</span></span>|<span data-ttu-id="4240a-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4240a-129">**Description**</span></span>|<span data-ttu-id="4240a-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="4240a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4240a-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="4240a-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="4240a-132">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="4240a-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4240a-133">opcional</span><span class="sxs-lookup"><span data-stu-id="4240a-133">optional</span></span>  <br/> |<span data-ttu-id="4240a-134">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="4240a-134">The default value is false.</span></span> <span data-ttu-id="4240a-135">Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="4240a-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="4240a-136">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="4240a-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4240a-137">Command</span><span class="sxs-lookup"><span data-stu-id="4240a-137">Command</span></span>  <br/> |<span data-ttu-id="4240a-138">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4240a-138">xsd:string</span></span>  <br/> |<span data-ttu-id="4240a-139">opcional</span><span class="sxs-lookup"><span data-stu-id="4240a-139">optional</span></span>  <br/> |<span data-ttu-id="4240a-140">A cadeia de caracteres de comando usada para consultar a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="4240a-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="4240a-141">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4240a-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4240a-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="4240a-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="4240a-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4240a-143">xsd:string</span></span>  <br/> |<span data-ttu-id="4240a-144">opcional</span><span class="sxs-lookup"><span data-stu-id="4240a-144">optional</span></span>  <br/> |<span data-ttu-id="4240a-145">A cadeia de caracteres de conexão que define os parâmetros necessários para se conectar a uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="4240a-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="4240a-146">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4240a-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4240a-147">FileName</span><span class="sxs-lookup"><span data-stu-id="4240a-147">FileName</span></span>  <br/> |<span data-ttu-id="4240a-148">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4240a-148">xsd:string</span></span>  <br/> |<span data-ttu-id="4240a-149">obrigatório</span><span class="sxs-lookup"><span data-stu-id="4240a-149">required</span></span>  <br/> |<span data-ttu-id="4240a-150">O nome do arquivo de conexão.</span><span class="sxs-lookup"><span data-stu-id="4240a-150">The name of the connection file.</span></span> <span data-ttu-id="4240a-151">Consulte Comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="4240a-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="4240a-152">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4240a-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4240a-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4240a-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="4240a-154">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4240a-154">xsd:string</span></span>  <br/> |<span data-ttu-id="4240a-155">opcional</span><span class="sxs-lookup"><span data-stu-id="4240a-155">optional</span></span>  <br/> |<span data-ttu-id="4240a-156">Um nome de usuário fornecido para a conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="4240a-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="4240a-157">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4240a-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4240a-158">ID</span><span class="sxs-lookup"><span data-stu-id="4240a-158">ID</span></span>  <br/> |<span data-ttu-id="4240a-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4240a-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4240a-160">obrigatório</span><span class="sxs-lookup"><span data-stu-id="4240a-160">required</span></span>  <br/> |<span data-ttu-id="4240a-161">O ID atribuído pelo Visio para uma determinada conexão, exclusivo dentro do documento.</span><span class="sxs-lookup"><span data-stu-id="4240a-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="4240a-162">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4240a-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4240a-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="4240a-163">Timeout</span></span>  <br/> |<span data-ttu-id="4240a-164">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4240a-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4240a-165">opcional</span><span class="sxs-lookup"><span data-stu-id="4240a-165">optional</span></span>  <br/> |<span data-ttu-id="4240a-166">O tempo de espera em minutos durante a tentativa de estabelecer uma conexão antes de abortar a tentativa.</span><span class="sxs-lookup"><span data-stu-id="4240a-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="4240a-167">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4240a-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

