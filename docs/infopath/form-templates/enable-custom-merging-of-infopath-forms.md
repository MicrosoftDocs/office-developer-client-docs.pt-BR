---
title: Habilitar a mesclagem personalizada de formulários do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: O recurso Mesclar Formulários do editor do Microsoft InfoPath foi projetado para combinar dados de vários formulários em um único formulário.
ms.openlocfilehash: 598c44bfe63a31237bf82ceb2212b001fbe7cc1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386912"
---
# <a name="enable-custom-merging-of-infopath-forms"></a><span data-ttu-id="cc8ea-103">Habilitar a mesclagem personalizada de formulários do InfoPath</span><span class="sxs-lookup"><span data-stu-id="cc8ea-103">Enable Custom Merging of InfoPath Forms</span></span>

<span data-ttu-id="cc8ea-104">O recurso **Mesclar Formulários** do editor do Microsoft InfoPath foi projetado para combinar dados de vários formulários em um único formulário,</span><span class="sxs-lookup"><span data-stu-id="cc8ea-104">The **Merge Forms** feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form.</span></span> <span data-ttu-id="cc8ea-105">o que também é conhecido como agregação de dados.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-105">This is also known as data aggregation.</span></span> <span data-ttu-id="cc8ea-106">Se a mesclagem de formulários estiver habilitada, você pode clicar na guia **Arquivo**, em **Salvar e Enviar**, em **Mesclar Formulários** sob **Importar e Vincular** e, em seguida, clicar no botão **Mesclar Formulários** para selecionar um ou mais formulários a mesclar com o formulário aberto no momento.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-106">If merging forms is enabled, you can click the **File** tab, click **Save &amp; Send**, click **Merge Forms** under **Import &amp; Link**, and then click the **Merge Forms** button to select one or more forms to merge with the currently opened form.</span></span> <span data-ttu-id="cc8ea-107">O formulário aberto no momento é o formulário de destino e os formulários selecionados na caixa de diálogo **Mesclar Formulários** são chamados de formulários de origem.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-107">The form that is currently open is the target form and the forms selected in the **Merge Forms** dialog box are known as the source forms.</span></span>
  
<span data-ttu-id="cc8ea-108">A agregação de dados resultante da mesclagem de formulários pode incluir todos os dados contidos nos formulários de origem e de destino ou apenas uma parte dos dados originais.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-108">The aggregation of data that results from merging forms can include all of the data that is contained in the source and target forms, or only a portion of the original data.</span></span> <span data-ttu-id="cc8ea-109">As operações padrão estão a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-109">The default operations are the following.</span></span>
  
- <span data-ttu-id="cc8ea-110">Para elementos que se repetem, os dados são inseridos em um local correspondente no documento de destino.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-110">For repeating elements, data is inserted at a matching location in the target document.</span></span> <span data-ttu-id="cc8ea-111">Isso ocorre quando o atributo **MaxOccurs** do elemento de destino for maior que 1.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-111">This happens when the **MaxOccurs** attribute of the destination element is greater than 1.</span></span> 
    
- <span data-ttu-id="cc8ea-112">Para elementos que não se repetem (ou seja, elementos em que **MaxOccurs** é "1"), os atributos dos elementos de origem são adicionados aos atributos existentes do elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-112">For non-repeating elements (that is, for elements where **MaxOccurs** is "1"), the attributes of the source elements are added to the existing attributes of the destination element.</span></span> 
    
## <a name="creating-a-custom-transform"></a><span data-ttu-id="cc8ea-113">Criar um cabeçalho personalizado</span><span class="sxs-lookup"><span data-stu-id="cc8ea-113">Creating a Custom Transform</span></span>

<span data-ttu-id="cc8ea-114">A operação padrão ao mesclar formulários funciona bem em formulários com base no mesmo esquema XML.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-114">The default operation when merging forms works well for forms that are based on the same XML schema.</span></span> <span data-ttu-id="cc8ea-115">Entretanto, em algumas circunstâncias, talvez você queira mesclar formulários com base em diferentes esquemas, ou substituir a operação de mesclagem padrão para formulários que tenham o mesmo esquema como base.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-115">In some circumstances, however, you may want to merge forms that are based on different schemas or override the default merge operation for forms that are based on the same schema.</span></span> <span data-ttu-id="cc8ea-116">Nesses cenários, você pode criar uma Transformação XSL (XSLT), que contém instruções de agregação para a operação de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-116">For these scenarios, you can create an XSL Transform (XSLT), which contains aggregation instructions for the merge operation.</span></span> <span data-ttu-id="cc8ea-117">A transformação é aplicada no momento da mesclagem para criar um documento DOM que contém as informações a importar, juntamente das anotações que especificam como incorporar essas informações no documento de destino.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-117">The transform is applied at merge time to create a DOM document that contains the information to be imported, together with annotations specifying how to incorporate this information into the target document.</span></span> <span data-ttu-id="cc8ea-118">Essas anotações são os atributos XML no namespace `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-118">These annotations are XML attributes in the namespace  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span></span>
  
<span data-ttu-id="cc8ea-119">Os atributos XML e seus valores servem como instruções de agregação sobre como cada nó é mesclado com o documento XML de destino.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-119">The XML attributes and their values serve as aggregation instructions on how each node is merged with the destination XML document.</span></span> <span data-ttu-id="cc8ea-120">Esses atributos são descritos nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-120">These attributes are described in the following sections.</span></span>
  
### <a name="select"></a><span data-ttu-id="cc8ea-121">select</span><span class="sxs-lookup"><span data-stu-id="cc8ea-121">select</span></span>

<span data-ttu-id="cc8ea-122">O atributo **agg:select** contém uma expressão XPath absoluta que identifica o elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-122">The **agg:select** attribute contains an absolute XPath expression which identifies the destination element.</span></span> 
  
### <a name="insert"></a><span data-ttu-id="cc8ea-123">insert</span><span class="sxs-lookup"><span data-stu-id="cc8ea-123">insert</span></span>

<span data-ttu-id="cc8ea-124">O valor de "insert" para o atributo **agg:action** instrui o InfoPath a inserir o elemento de origem como filho do elemento de destino especificado usando o atributo **agg:select**.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-124">A value of "insert" for the **agg:action** attribute instructs InfoPath to insert the source element as a child of the destination element that is specified by using the **agg:select** attribute.</span></span> <span data-ttu-id="cc8ea-125">Os filhos do elemento de origem são incluídos na operação de inserção.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-125">The children of the source element are included in the insert operation.</span></span> <span data-ttu-id="cc8ea-126">O atributo **selectChild** permite que você selecione um determinado local para a operação do nó de inserção.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-126">The **selectChild** attribute lets you select a certain location for the insert node operation.</span></span> <span data-ttu-id="cc8ea-127">O atributo **order** é usado para especificar se os elementos de origem são inseridos antes ou depois dos elementos de destino existentes.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-127">The **order** attribute is used to specify whether the source elements are inserted before existing destination elements or after.</span></span> <span data-ttu-id="cc8ea-128">O valor padrão é "depois" se o atributo **order** não estiver presente.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-128">The default value if the **order** attribute is not present is "after".</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a><span data-ttu-id="cc8ea-129">replace</span><span class="sxs-lookup"><span data-stu-id="cc8ea-129">replace</span></span>

<span data-ttu-id="cc8ea-130">O valor de "replace" para o atributo **agg:action** instrui o InfoPath a substituir cada um dos elementos de destino citados pelo atributo **select** pelo elemento de origem.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-130">A value of "replace" for the **agg:action** attribute instructs InfoPath to replace each of the destination elements referred to by the **select** attribute with the source element.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a><span data-ttu-id="cc8ea-131">mergeAttributes</span><span class="sxs-lookup"><span data-stu-id="cc8ea-131">mergeAttributes</span></span>

<span data-ttu-id="cc8ea-132">Se o valor do atributo **agg:action** for "mergeAttributes", os atributos do elemento de origem são mesclados aos atributos de cada um dos elementos de destino citados pelo atributo **select**.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-132">If the value of the **agg:action** attribute is "mergeAttributes", the attributes of the source element are merged with the attributes of each of the destination elements referred to by the **select** attribute.</span></span> 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a><span data-ttu-id="cc8ea-133">delete</span><span class="sxs-lookup"><span data-stu-id="cc8ea-133">delete</span></span>

<span data-ttu-id="cc8ea-134">Se o valor do atributo **agg:action** for "delete", todos os elementos de destino citados pelo atributo **select** serão excluídos do documento de destino.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-134">If the value of the **agg:action** attribute is "delete", each of the destination elements referred to by the **select** attribute are deleted from the destination document.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

<span data-ttu-id="cc8ea-135">Junto aos atributos especificados no namespace `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`, use o namespace `https://schemas.microsoft.com/office/infopath/2003/aggregation-target` para indicar um objeto XSL que implementa a interface **IXMLDOMDocument**.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-135">In conjunction with the attributes specified in the  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation` namespace, you use the  `https://schemas.microsoft.com/office/infopath/2003/aggregation-target` namespace to denote an XSL object that implements the interface **IXMLDOMDocument**.</span></span> <span data-ttu-id="cc8ea-136">Um dos membros mais úteis dessa interface é o método **get-documentElement**.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-136">One of the most useful members of this interface is the method **get-documentElement**.</span></span>
  
### <a name="get-documentelement"></a><span data-ttu-id="cc8ea-137">get-documentElement</span><span class="sxs-lookup"><span data-stu-id="cc8ea-137">get-documentElement</span></span>

<span data-ttu-id="cc8ea-138">A função **target:get-documentElement** fornece acesso ao Modelo de Objeto do Documento de destino.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-138">The **target:get-documentElement** function provides access to the Document Object Model of the destination document.</span></span> <span data-ttu-id="cc8ea-139">Ela pode ser usada para alterar a maneira como a operação de mesclagem funciona com base no conteúdo atual do documento de destino.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-139">It can be used to change the way the merge operation works based on the current contents of the destination document.</span></span> 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a><span data-ttu-id="cc8ea-140">Etapas para criar uma mesclagem personalizada</span><span class="sxs-lookup"><span data-stu-id="cc8ea-140">Steps for Creating a Custom Merge</span></span>

1. <span data-ttu-id="cc8ea-141">Selecione os tipos de documentos XML de origem dos quais você deseja mesclar os dados.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-141">Select the kinds of XML source documents from which you want to merge data.</span></span> <span data-ttu-id="cc8ea-142">Colete uma amostra representativa de cada tipo de documento de origem.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-142">Collect a representative sample of each kind of source document.</span></span>
    
2. <span data-ttu-id="cc8ea-143">Obtenha o esquema XML para cada tipo de documento XML de origem para um formulário existente do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-143">Derive the XML schema for each kind of XML source document for an existing InfoPath form.</span></span> <span data-ttu-id="cc8ea-144">Esta etapa é realizada com facilidade exportando o esquema XML com o comando **Exportar Arquivos de Origem** na guia **Publicar** do modo de exibição Backstage.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-144">This step is easily accomplished by exporting the XML schema with the **Export Source Files** command on the **Publish** tab of the Backstage.</span></span> <span data-ttu-id="cc8ea-145">Para documentos XML que não foram criados no InfoPath, você pode usar uma ferramenta como o Microsoft Visual Studio para criar um esquema do documento XML de exemplo, ou pode criar um formulário de exemplo a partir de um documento XML do InfoPath e exportar o esquema que o InfoPath obtém a partir da estrutura do documento.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-145">For XML documents that were not created in InfoPath, you can use a tool such as Microsoft Visual Studio to create a schema from the sample XML document, or you can create a sample form from the XML document in InfoPath, and then export the schema that InfoPath derives from the document structure.</span></span> 
    
3. <span data-ttu-id="cc8ea-146">Identifique os dados que você deseja mesclar em cada tipo de documento XML de origem.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-146">Identify the data that you want to merge from each kind of XML source document.</span></span> <span data-ttu-id="cc8ea-147">Esta etapa depende quase completamente dos requisitos dos formulários de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-147">This step will depend almost entirely on the requirements of both your source and destination forms.</span></span> <span data-ttu-id="cc8ea-148">Em alguns formulários, convém copiar todos os dados do formulário de origem.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-148">For some forms, you may want to copy all of the data from the source form.</span></span> <span data-ttu-id="cc8ea-149">Em outros, talvez você queira apenas um ou dois elementos do documento XML subjacente do formulário.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-149">For others, you may want only one or two elements from the form's underlying XML document.</span></span> <span data-ttu-id="cc8ea-150">Ao identificar quais são os dados que você deseja mesclar, preste atenção aos documentos de origem e de destino para garantir que os elementos mapeiem logicamente os dois formulários.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-150">When identifying what data that you want to merge, pay extra attention to both the source and destination documents to ensure that the elements map logically between the two forms.</span></span>
    
4. <span data-ttu-id="cc8ea-151">Crie uma transformação XSL para cada tipo de documento XML de origem.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-151">Create an XSL transform for each kind of XML source document.</span></span> <span data-ttu-id="cc8ea-152">Ao configurar a mesclagem de formulários, será esta etapa que levará mais tempo.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-152">When configuring the merging of your forms, this step will take the most time.</span></span> <span data-ttu-id="cc8ea-153">O propósito da transformação XSL é transformar o documento XML de origem em um formato que possa ser mesclado com o formulário de destino.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-153">The purpose of the XSL transform is to transform the source XML document into a format that can be merged with the destination form.</span></span> <span data-ttu-id="cc8ea-154">Ao criar a transformação, decida se quer usar a mesclagem de caminhos de locais de XML ou mesclar a partir das instruções de agregação do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-154">When designing your transform, decide whether you want to use merging from XML location paths, or merging from InfoPath aggregation instructions.</span></span>
    
    <span data-ttu-id="cc8ea-155">O Visual Studio é uma ferramenta conveniente para criar transformações XSL.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-155">Visual Studio is a convenient tool for creating XSL transforms.</span></span> <span data-ttu-id="cc8ea-156">O Visual Studio fornece uma estrutura de tópicos do documento e cores de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-156">Visual Studio provides syntax coloring and a document outline.</span></span> <span data-ttu-id="cc8ea-157">Também fornece automaticamente o fechamento de marcas para elementos XSL, o que pode ajudar a diminuir a digitação redundante e erros de ortografia difíceis de encontrar.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-157">It also automatically provides closing tags for your XSL elements, which can help decrease redundant typing and hard-to-find spelling errors.</span></span> <span data-ttu-id="cc8ea-158">Você também pode criar transformações XSL com um editor de texto, como o Bloco de Notas.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-158">You can also create XSL transforms with a text editor such as Notepad.</span></span>
    
    <span data-ttu-id="cc8ea-159">Comece com a transformação da identidade, que é simplesmente uma transformação XSL que gera o mesmo arquivo XML de entrada:</span><span class="sxs-lookup"><span data-stu-id="cc8ea-159">Start with the identity transform, which is simply an XSL transform that outputs the same XML file that is input:</span></span>
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="https://www.w3.org/1999/XSL/Transform" 
        xmlns:agg="https://schemas.microsoft.com/office/infopath/2003/aggregation" 
        xmlns:target="https://schemas.microsoft.com/office/infopath/2003/aggregation-target" 
        xmlns:my="https://schemas.microsoft.com/office/infopath/2003/myXSD/2003-05-29T20:30:47"> 
            <xsl:template match="/"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
            <xsl:template match="@* | node()"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
        </xsl:stylesheet>
    ```

    <span data-ttu-id="cc8ea-160">Depois adicione seções de substituição do modelo para os elementos aos quais você deseja adicionar um tratamento especial.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-160">Then add overriding template sections for the elements you want to add special handling for.</span></span> <span data-ttu-id="cc8ea-161">Por exemplo, este modelo altera o elemento `<src:Task>` no elemento `<my:field1>` e define o valor do atributo **agg:action** como "replace".</span><span class="sxs-lookup"><span data-stu-id="cc8ea-161">For example, this template changes a  `<src:Task>` element into a  `<my:field1>` element and sets the value of the **agg:action** attribute to "replace".</span></span> 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. <span data-ttu-id="cc8ea-162">Adicione arquivos de transformação XSL e de esquema ao modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-162">Add the XSL transform files and schema files in the form template.</span></span> <span data-ttu-id="cc8ea-163">Depois de obter os esquemas para cada tipo de documento de origem e criar uma transformação XSL para converter cada tipo de documento para que o InfoPath possa mesclar os dados, adicione-os como recursos ao seu formulário.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-163">After you have derived schemas for each kind of source document and created an XSL transform to convert each document type so that InfoPath can merge its data, add them to as resources to your form.</span></span> <span data-ttu-id="cc8ea-164">Clique em **Arquivos de Recurso** na guia **Dados** e, em seguida, clique em **Adicionar** na caixa de diálogo **Arquivos de Recurso**, navegue até o arquivo de esquema ou transformação XSL e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-164">Click **Resource Files** on the **Data** tab, and then click **Add** in the **Resource Files** dialog box, browse to your schema or XSL transform file, and then click **OK**.</span></span> <span data-ttu-id="cc8ea-165">Faça isso para cada arquivo de esquema e de transformação XSL que você criou.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-165">Do this to for each schema file and XSL transform file that you created.</span></span>
    
    <span data-ttu-id="cc8ea-166">Se os esquemas que você adicionou usam o atributo **targetNamespace**, é necessário adicionar um elemento de propriedade ao arquivo .xsf do formulário para que o InfoPath saiba o namespace do esquema.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-166">If the schemas that you add use the **targetNamespace** attribute, you must add a property element to the form's .xsf file so that InfoPath knows the namespace of the schema.</span></span> <span data-ttu-id="cc8ea-167">Para acessar esse arquivo, clique na guia **Arquivo**, em **Publicar** e em **Exportar Arquivos de Origem**.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-167">To access this file, click the **File** tab, click **Publish**, and then click **Export Source Files**.</span></span> <span data-ttu-id="cc8ea-168">Selecione o local dos arquivos e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-168">Select a location for the files, and then click **OK**.</span></span> <span data-ttu-id="cc8ea-169">Feche o modelo de formulário do InfoPath que você está desenvolvendo.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-169">Then close the InfoPath form template that you are designing.</span></span>
    
    <span data-ttu-id="cc8ea-170">Navegue até o local especificado para os arquivos extraídos e localize o arquivo com extensão de nome .xsf.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-170">Browse to the location that you specified for the extracted files and find the file that has an .xsf file name extension.</span></span> <span data-ttu-id="cc8ea-171">Normalmente, esse arquivo chama-se manifest.xsf.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-171">Usually, this file is called manifest.xsf.</span></span> <span data-ttu-id="cc8ea-172">Abra o arquivo no Bloco de Notas, encontre a marca `<xsf:file>` que corresponde ao seu esquema e adicione um elemento de propriedade "namespace" para especificar o **targetNamespace** como mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-172">Open the file in Notepad, find the  `<xsf:file>` tag that corresponds to your schema, and add a "namespace" property element to specify the **targetNamespace** as shown in the following example.</span></span> 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. <span data-ttu-id="cc8ea-173">A última etapa ao preparar seu formulário para oferecer suporte à mesclagem personalizada é atualizar o elemento **importParameters** no arquivo .xsf associado ao formulário.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-173">The last step in preparing your form to support custom merging is to update the **importParameters** element in the .xsf file associated with the form.</span></span> 

    <span data-ttu-id="cc8ea-174">Primeiro, localize a marca `<xsf:importParameters>` no arquivo .xsf.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-174">First, find the  `<xsf:importParameters>` tag in the .xsf file.</span></span> <span data-ttu-id="cc8ea-175">Para cada par de esquema/transformação XSL que você criou para seu formulário, adicione um elemento **xsf:importSource** ao elemento **xsf:importParameters**: `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-175">For each schema/XSL transform pair you have created for your form, add an **xsf:importSource** element to the **xsf:importParameters** element:  `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span></span> 
    
    <span data-ttu-id="cc8ea-176">O atributo **name** do elemento **xsf:importSource** contém o nome do modelo de formulário que pode ser encontrado em um documento XML de origem.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-176">The **name** attribute of the **xsf:importSource** element contains the form template's name that may be found in a source XML document.</span></span> <span data-ttu-id="cc8ea-177">Normalmente, você pode deixá-lo em branco.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-177">Usually, you can leave this empty.</span></span> <span data-ttu-id="cc8ea-178">O atributo **schema** contém o nome de um arquivo de esquema adicionado ao modelo de formulário na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-178">The **schema** attribute contains the name of a schema file that you added to the form template in the previous step.</span></span> <span data-ttu-id="cc8ea-179">Por fim, o atributo **transform** contém o nome da transformação XSL que você deseja usar para converter os formulários que estão de acordo com o esquema.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-179">Finally, the **transform** attribute contains the name of the XSL transform that you want to use to convert forms that conform to the schema.</span></span> 
    
    <span data-ttu-id="cc8ea-180">Você pode usar uma transformação personalizada com o evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) ou por conta própria.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-180">You can use a custom transform either with the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event or on its own.</span></span> 
    
## <a name="creating-a-custom-merge-in-code"></a><span data-ttu-id="cc8ea-181">Criar uma mesclagem personalizada com código</span><span class="sxs-lookup"><span data-stu-id="cc8ea-181">Creating a Custom Merge in Code</span></span>

<span data-ttu-id="cc8ea-182">A mesclagem personalizada com código é compatível com o uso do manipulador de eventos [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx), com seu atributo **useScriptHandler** correspondente do elemento **importParameters** no arquivo .xsf associado ao formulário.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-182">Custom merging with code is supported by using the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event handler, with its corresponding **useScriptHandler** attribute of the **importParameters** element in the .xsf file associated with the form.</span></span> 

<span data-ttu-id="cc8ea-183">No código gerenciado, você pode habilitar o evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) marcando a caixa **Mesclar usando código personalizado** e, em seguida, clicando no botão **Editar**, na categoria **Avançado** da caixa de diálogo **Opções de Formulário** disponível no modo de exibição Backstage.</span><span class="sxs-lookup"><span data-stu-id="cc8ea-183">In managed code, you can enable the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event by checking the box **Merge using custom code**, and then clicking the **Edit** button, in the **Advanced** category of the **Form Options** dialog box available from the Backstage.</span></span> 
  

