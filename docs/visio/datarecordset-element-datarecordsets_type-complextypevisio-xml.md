---
title: Elemento de DataRecordSet (DataRecordSets_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Armazena, formata, atualiza e expõe os dados consultados de um banco de dados no Microsoft Visio.
ms.openlocfilehash: 157213476214c736367b724dd6ca944060c53467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771662"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="f04d7-103">Elemento de DataRecordSet (DataRecordSets_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f04d7-103">DataRecordSet element (DataRecordSets_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f04d7-104">Armazena, formata, atualiza e expõe os dados consultados de um banco de dados no Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="f04d7-104">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f04d7-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="f04d7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f04d7-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="f04d7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f04d7-107">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="f04d7-107">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f04d7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f04d7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f04d7-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f04d7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f04d7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f04d7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f04d7-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="f04d7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f04d7-112">Recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="f04d7-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f04d7-113">Definição</span><span class="sxs-lookup"><span data-stu-id="f04d7-113">Definition</span></span>

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f04d7-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f04d7-114">Elements and attributes</span></span>

<span data-ttu-id="f04d7-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f04d7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f04d7-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="f04d7-116">Parent elements</span></span>

|<span data-ttu-id="f04d7-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f04d7-117">**Element**</span></span>|<span data-ttu-id="f04d7-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f04d7-118">**Type**</span></span>|<span data-ttu-id="f04d7-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f04d7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f04d7-120">DataRecordSets</span><span class="sxs-lookup"><span data-stu-id="f04d7-120">DataRecordSets</span></span>](datarecordsets-elementvisio-xml.md) <br/> |[<span data-ttu-id="f04d7-121">DataRecordSets_Type</span><span class="sxs-lookup"><span data-stu-id="f04d7-121">DataRecordSets_Type</span></span>](datarecordsets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f04d7-122">Contém todos os elementos de **DataRecordset** no documento.</span><span class="sxs-lookup"><span data-stu-id="f04d7-122">Contains all the **DataRecordset** elements in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f04d7-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f04d7-123">Child elements</span></span>

|<span data-ttu-id="f04d7-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f04d7-124">**Element**</span></span>|<span data-ttu-id="f04d7-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f04d7-125">**Type**</span></span>|<span data-ttu-id="f04d7-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f04d7-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f04d7-127">ADOData</span><span class="sxs-lookup"><span data-stu-id="f04d7-127">ADOData</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f04d7-128">ADOData_Type</span><span class="sxs-lookup"><span data-stu-id="f04d7-128">ADOData_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f04d7-129">Contém o XML que está em conformidade com o esquema XML clássico do ADO para um recordset do ADO e que descreve os dados no conjunto de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="f04d7-129">Contains XML that conforms to the ADO classic XML schema for an ADO recordset and that describes the data in the data recordset.</span></span>  <br/> |
|[<span data-ttu-id="f04d7-130">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="f04d7-130">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f04d7-131">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="f04d7-131">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f04d7-132">Define uma regra que compara uma coluna no elemento pai **DataRecordset** com um item de dados da forma da última bem-sucedida automática vinculação ação executada na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f04d7-132">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span>  <br/> |
|[<span data-ttu-id="f04d7-133">DataColumn</span><span class="sxs-lookup"><span data-stu-id="f04d7-133">DataColumn</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f04d7-134">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="f04d7-134">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f04d7-135">Define como uma coluna de dados aparece na janela **Dados externos** na interface do usuário do Visio e qualifica os dados na coluna definindo seu tipo de dados e formatação.</span><span class="sxs-lookup"><span data-stu-id="f04d7-135">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
|[<span data-ttu-id="f04d7-136">DataColumns</span><span class="sxs-lookup"><span data-stu-id="f04d7-136">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f04d7-137">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="f04d7-137">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f04d7-138">Contém todos os elementos de **DataColumn** em um conjunto de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="f04d7-138">Contains all the **DataColumn** elements in a data recordset.</span></span>  <br/> |
|[<span data-ttu-id="f04d7-139">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="f04d7-139">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f04d7-140">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="f04d7-140">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f04d7-141">Identifica um ou mais colunas de chave primária no conjunto de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="f04d7-141">Identifies one or more primary-key columns in the data recordset.</span></span>  <br/> |
|[<span data-ttu-id="f04d7-142">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="f04d7-142">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f04d7-143">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="f04d7-143">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f04d7-144">Indica uma linha no conjunto de registros de dados vinculada a uma forma que está em conflito após a atualização dos registros de dados.</span><span class="sxs-lookup"><span data-stu-id="f04d7-144">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>  <br/> |
|[<span data-ttu-id="f04d7-145">RowMap</span><span class="sxs-lookup"><span data-stu-id="f04d7-145">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f04d7-146">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="f04d7-146">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f04d7-147">Mapeia uma linha do conjunto de registros de dados a uma forma.</span><span class="sxs-lookup"><span data-stu-id="f04d7-147">Maps a data-recordset row to a shape.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f04d7-148">Atributos</span><span class="sxs-lookup"><span data-stu-id="f04d7-148">Attributes</span></span>

|<span data-ttu-id="f04d7-149">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f04d7-149">**Attribute**</span></span>|<span data-ttu-id="f04d7-150">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f04d7-150">**Type**</span></span>|<span data-ttu-id="f04d7-151">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f04d7-151">**Required**</span></span>|<span data-ttu-id="f04d7-152">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f04d7-152">**Description**</span></span>|<span data-ttu-id="f04d7-153">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f04d7-153">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f04d7-154">Soma de verificação</span><span class="sxs-lookup"><span data-stu-id="f04d7-154">Checksum</span></span>  <br/> |<span data-ttu-id="f04d7-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f04d7-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f04d7-156">opcional</span><span class="sxs-lookup"><span data-stu-id="f04d7-156">optional</span></span>  <br/> |<span data-ttu-id="f04d7-157">Um valor de soma de verificação, geradas pelo Visio e com base nas propriedades do conjunto de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="f04d7-157">A checksum value, generated by Visio, and based on data-recordset properties.</span></span> <span data-ttu-id="f04d7-158">Defina este attirbute como 0; O Visio recalcula esse valor em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f04d7-158">Set this attirbute to 0; Visio recalculates this value at runtime.</span></span>  <br/> |<span data-ttu-id="f04d7-159">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f04d7-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f04d7-160">Comando</span><span class="sxs-lookup"><span data-stu-id="f04d7-160">Command</span></span>  <br/> |<span data-ttu-id="f04d7-161">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f04d7-161">xsd:string</span></span>  <br/> |<span data-ttu-id="f04d7-162">opcional</span><span class="sxs-lookup"><span data-stu-id="f04d7-162">optional</span></span>  <br/> |<span data-ttu-id="f04d7-163">A cadeia de caracteres de comando usada para dados de consulta da fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="f04d7-163">The command string used to query data from the data source.</span></span>  <br/> |<span data-ttu-id="f04d7-164">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f04d7-164">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f04d7-165">Conexão</span><span class="sxs-lookup"><span data-stu-id="f04d7-165">ConnectionID</span></span>  <br/> |<span data-ttu-id="f04d7-166">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f04d7-166">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f04d7-167">opcional</span><span class="sxs-lookup"><span data-stu-id="f04d7-167">optional</span></span>  <br/> |<span data-ttu-id="f04d7-168">A identificação de conexão para o objeto **DataConnection** associado.</span><span class="sxs-lookup"><span data-stu-id="f04d7-168">The connection ID for the associated **DataConnection** object.</span></span> <span data-ttu-id="f04d7-169">Não existe para fontes de dados XML.</span><span class="sxs-lookup"><span data-stu-id="f04d7-169">Does not exist for XML data sources.</span></span>  <br/> |<span data-ttu-id="f04d7-170">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f04d7-170">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f04d7-171">Id</span><span class="sxs-lookup"><span data-stu-id="f04d7-171">ID</span></span>  <br/> |<span data-ttu-id="f04d7-172">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f04d7-172">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f04d7-173">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f04d7-173">required</span></span>  <br/> |<span data-ttu-id="f04d7-174">A identificação de recordset dados, exclusiva dentro do documento.</span><span class="sxs-lookup"><span data-stu-id="f04d7-174">The data recordset ID, unique within the document.</span></span>  <br/> |<span data-ttu-id="f04d7-175">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f04d7-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f04d7-176">Nome</span><span class="sxs-lookup"><span data-stu-id="f04d7-176">Name</span></span>  <br/> |<span data-ttu-id="f04d7-177">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f04d7-177">xsd:string</span></span>  <br/> |<span data-ttu-id="f04d7-178">opcional</span><span class="sxs-lookup"><span data-stu-id="f04d7-178">optional</span></span>  <br/> |<span data-ttu-id="f04d7-179">A exibição (ou "amigável") nome do conjunto de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="f04d7-179">The display (or "friendly") name of the data recordset.</span></span>  <br/> |<span data-ttu-id="f04d7-180">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f04d7-180">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f04d7-181">NextRowID</span><span class="sxs-lookup"><span data-stu-id="f04d7-181">NextRowID</span></span>  <br/> |<span data-ttu-id="f04d7-182">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f04d7-182">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f04d7-183">opcional</span><span class="sxs-lookup"><span data-stu-id="f04d7-183">optional</span></span>  <br/> |<span data-ttu-id="f04d7-184">O próximo disponíveis Visio identificação da linha.</span><span class="sxs-lookup"><span data-stu-id="f04d7-184">The next available Visio row ID.</span></span>  <br/> |<span data-ttu-id="f04d7-185">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f04d7-185">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f04d7-186">Options</span><span class="sxs-lookup"><span data-stu-id="f04d7-186">Options</span></span>  <br/> |<span data-ttu-id="f04d7-187">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f04d7-187">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f04d7-188">opcional</span><span class="sxs-lookup"><span data-stu-id="f04d7-188">optional</span></span>  <br/> |<span data-ttu-id="f04d7-189">Opções que se aplicam ao conjunto de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="f04d7-189">Options to apply to the data recordset.</span></span> <span data-ttu-id="f04d7-190">Os valores possíveis podem ser qualquer combinação de um ou mais daqueles mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f04d7-190">Possible values can be any combination of one or more of those shown in the following table.</span></span>  <br/> |<span data-ttu-id="f04d7-191">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f04d7-191">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f04d7-192">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="f04d7-192">RefreshInterval</span></span>  <br/> |<span data-ttu-id="f04d7-193">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f04d7-193">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f04d7-194">opcional</span><span class="sxs-lookup"><span data-stu-id="f04d7-194">optional</span></span>  <br/> |<span data-ttu-id="f04d7-195">Frequência (em minutos) Visio atualiza automaticamente o conjunto de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="f04d7-195">How often (in minutes) Visio refreshes the data recordset automatically.</span></span> <span data-ttu-id="f04d7-196">Este valor deve ser 1 ou maior.</span><span class="sxs-lookup"><span data-stu-id="f04d7-196">This value must be 1 or larger.</span></span>  <br/> |<span data-ttu-id="f04d7-197">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f04d7-197">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f04d7-198">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="f04d7-198">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="f04d7-199">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="f04d7-199">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f04d7-200">opcional</span><span class="sxs-lookup"><span data-stu-id="f04d7-200">optional</span></span>  <br/> |<span data-ttu-id="f04d7-201">Se a interface do usuário reconciliação de dados deve ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="f04d7-201">Whether the data-reconciliation user interface should be disabled.</span></span> <span data-ttu-id="f04d7-202">True (1) para desativar a interface de usuário (UI).</span><span class="sxs-lookup"><span data-stu-id="f04d7-202">True (1) to disable the user interface (UI).</span></span> <span data-ttu-id="f04d7-203">False (0) para habilitar a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f04d7-203">False (0) to enable the UI.</span></span>  <br/> |<span data-ttu-id="f04d7-204">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f04d7-204">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f04d7-205">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="f04d7-205">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="f04d7-206">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="f04d7-206">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f04d7-207">opcional</span><span class="sxs-lookup"><span data-stu-id="f04d7-207">optional</span></span>  <br/> |<span data-ttu-id="f04d7-208">Se deseja substituir alterações do usuário a itens de dados da forma em formas vinculadas aos dados quando o conjunto de registros de dados for atualizado.</span><span class="sxs-lookup"><span data-stu-id="f04d7-208">Whether to overwrite user changes to shape data items in shapes linked to data when the data recordset is refreshed.</span></span>  <br/> |<span data-ttu-id="f04d7-209">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f04d7-209">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f04d7-210">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="f04d7-210">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="f04d7-211">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f04d7-211">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f04d7-212">opcional</span><span class="sxs-lookup"><span data-stu-id="f04d7-212">optional</span></span>  <br/> |<span data-ttu-id="f04d7-213">Define como os vínculos forma-dados são tratados quando as formas são copiadas ou recortadas.</span><span class="sxs-lookup"><span data-stu-id="f04d7-213">Defines how shape-data links are treated when shapes are copied or cut.</span></span> <span data-ttu-id="f04d7-214">1 para substituir os vínculos existentes na forma de destino.</span><span class="sxs-lookup"><span data-stu-id="f04d7-214">1 to replace existing links in the target shape.</span></span> <span data-ttu-id="f04d7-215">0 para manter os vínculos existentes na forma de destino.</span><span class="sxs-lookup"><span data-stu-id="f04d7-215">0 to maintain existing links in the target shape.</span></span>  <br/> |<span data-ttu-id="f04d7-216">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f04d7-216">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f04d7-217">RowOrder</span><span class="sxs-lookup"><span data-stu-id="f04d7-217">RowOrder</span></span>  <br/> |<span data-ttu-id="f04d7-218">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="f04d7-218">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f04d7-219">opcional</span><span class="sxs-lookup"><span data-stu-id="f04d7-219">optional</span></span>  <br/> |<span data-ttu-id="f04d7-220">Se usar a ordem das linhas no conjunto de registros de dados como a chave primária.</span><span class="sxs-lookup"><span data-stu-id="f04d7-220">Whether to use the order of the rows in the data recordset as the primary key.</span></span> <span data-ttu-id="f04d7-221">True (1) se a linha IDs são determinados pelo ordem da linha.</span><span class="sxs-lookup"><span data-stu-id="f04d7-221">True (1) if row IDs are determined by row order.</span></span> <span data-ttu-id="f04d7-222">False (0) se a linha IDs são determinados pelos valores das colunas de chave primária de registros de dados.</span><span class="sxs-lookup"><span data-stu-id="f04d7-222">False (0) if row IDs are determined by values in the primary key column(s) of the data recordset.</span></span>  <br/> |<span data-ttu-id="f04d7-223">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f04d7-223">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f04d7-224">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="f04d7-224">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="f04d7-225">XSD: DateTime</span><span class="sxs-lookup"><span data-stu-id="f04d7-225">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="f04d7-226">opcional</span><span class="sxs-lookup"><span data-stu-id="f04d7-226">optional</span></span>  <br/> |<span data-ttu-id="f04d7-227">A data e hora que o conjunto de registros de dados foi atualizado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="f04d7-227">The date and time the data recordset was last refreshed.</span></span>  <br/> |<span data-ttu-id="f04d7-228">Valores do tipo xsd: DateTime.</span><span class="sxs-lookup"><span data-stu-id="f04d7-228">Values of the xsd:dateTime type.</span></span>  <br/> |
   
